# Tech Stack

This lists the technology we plan to use and why. Items marked **option** are candidates that will be confirmed during Phase 0, once partner constraints are known.

## Blockchain layer

| Choice | Why |
|---|---|
| EVM-compatible, low-fee public chain (option: an Ethereum layer 2 such as Base) | Cheap and fast settlement, mature tooling, wide wallet and stablecoin support |
| Regulated, fully reserved stablecoin (option: a major USD stablecoin) | Stable value in transit, wide on-ramp and off-ramp support, lower depeg risk than algorithmic coins |
| Solidity smart contracts | The standard for EVM escrow logic |
| Foundry | Fast testing, fuzzing and invariant tests for the escrow rules |

## Backend

| Choice | Why |
|---|---|
| TypeScript on Node.js | One language across backend and app, strong typing for money logic |
| viem | Typed, lightweight library for reading and writing the chain |
| A relational database such as PostgreSQL (option) | Users, quotes and transfer status need durable, queryable storage |
| A message provider for SMS or chat (option) | Delivers the one-time code to a basic phone |

## Apps

| Choice | Why |
|---|---|
| React with a mobile-first progressive web app | One codebase, no app store needed for the pilot, works on low-end phones |
| Multi-language support from the start | Senders and receivers use different languages |

## Compliance and payments (partners, not built in-house)

| Need | Approach |
|---|---|
| Licensed cross-border transfer | Operate through a licensed Singapore partner first |
| SGD to stablecoin on-ramp | Licensed on-ramp provider |
| Stablecoin to local currency off-ramp | Philippines cash-out partner, mobile wallet or agent network |
| Identity checks and AML monitoring | Third-party KYC and AML provider |

## Security and operations

- Keys for any operator wallets held in managed key storage, never in code.
- An independent smart contract audit before real funds.
- Monitoring and alerting on stuck transfers and failed settlements.
- Rate and fee quotes recorded with each transfer so receipts can be audited.

## Why not a normal database or bank rails alone?

- A private database lets the provider keep margins opaque. A public ledger makes the fee and rate checkable.
- Escrow with automatic refund needs a trusted party if it is not enforced by code.
- Correspondent banking adds the intermediary layers that create the cost we want to remove.
- Open rails let any licensed agent join and compete on price.

## What the chain does and does not do

The chain provides cheap settlement, programmable escrow and a tamper-evident record. It does not replace licensing, identity checks or the cash-out network. Those stay with licensed partners.
