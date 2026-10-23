# How to Build

This document describes how the first working version (the pilot product) would be built. It is a plan, not a record of finished work.

## Scope of the first version

In scope:
- A sender app for workers in Singapore: enter an amount, see the exact amount the family will receive, confirm, track.
- A receiver flow for the family in the Philippines: receive a one-time code or QR, collect as local currency in a mobile wallet or as cash at a partner agent.
- An escrow smart contract that holds the transfer until it is collected, and refunds the sender automatically if it is not.
- A public receipt for each transfer showing the amount sent, the fee, the rate used and the amount received.

Out of scope for the first version: other corridors, our own licence, a custom wallet, advanced agent tooling.

## System overview

```
Sender app  ->  Backend  ->  On-ramp partner (SGD to stablecoin)
                  |
                  v
            Escrow contract  <-  Cash-out partner / agent (collects with code)
                  |
                  v
           Public receipt (events)  ->  Sender and receiver apps
```

## Components

### 1. Escrow smart contract
Holds the stablecoin for each transfer and enforces the rules in code.

- `createTransfer`: the sender (or the backend on their behalf) locks an amount of stablecoin with a hash of a one-time collection code and an expiry time.
- `collect`: the cash-out partner presents the code. The contract checks it against the stored hash and releases the funds to the partner's settlement address, who then pays the family in local currency.
- `refund`: after the expiry time, the sender can pull the funds back if they were never collected.
- Events: each step emits an event containing the transfer id, amount, fee and the quoted rate, so the public receipt can be rebuilt by anyone from the chain.

Design notes:
- Store only a hash of the collection code, never the code.
- Use pseudonymous transfer ids. Do not put names or phone numbers on a public chain.
- Update state before moving funds, and test the refund and double-collect paths carefully.

### 2. Backend service
- Quotes the transfer: converts SGD to the local amount, adds the fee, and shows the result before the sender confirms.
- Talks to the licensed on-ramp partner to turn SGD into stablecoin.
- Creates the transfer on-chain and generates the one-time code.
- Notifies the receiver by message and tracks status.
- Handles KYC checks through the compliance provider.

### 3. Sender app
A simple mobile-first web app (installable as a progressive web app). Screens: sign in and identity check, enter amount, review quote, confirm, track, receipt.

### 4. Receiver flow
Works on a basic phone: a message with a one-time code or QR, and clear steps to collect from a mobile wallet or a nearby agent.

### 5. Cash-out partner integration
A small interface for the partner to verify a code, mark a collection, and settle. Start with one partner and a manual or semi-manual process, then automate.

## Build order

1. **Contract first.** Write the escrow contract and a full test suite for collect, refund, expiry, double-collect, and wrong-code cases.
2. **Quote and receipt logic.** Build the backend quote and the public receipt from chain events.
3. **Sender app.** Connect the app to the backend and the test network.
4. **Receiver and agent flow.** Build the code or QR collection with a test partner.
5. **On-ramp and compliance.** Integrate the licensed partner and KYC in a sandbox.
6. **End-to-end test.** Run a full transfer on a test network with test money and test partners.
7. **Closed pilot.** Move to real partners and a small invited group.

## Testing

- Contract unit tests and invariant tests (funds in equal funds out, no transfer can be both collected and refunded).
- End-to-end tests of the full send, collect and refund flows on a test network.
- Usability tests with real workers and families before the pilot.
- An independent security review of the contract before it holds real funds.

## Definition of done for the pilot product

- A worker can complete a transfer without understanding blockchains.
- Every transfer ends either collected or refunded, with no stuck funds.
- The receipt shows the same numbers the worker saw before confirming.
- The all-in cost can be measured for every transfer.
