# Remittance Rail

**Send money home in minutes, and see exactly where every cent went.**

Idea Track submission for the Web3 for Social Good Hackathon 2026.

[Pitch deck](pitch/index.html): open the file in a browser and use the arrow keys.

---

## The problem

Migrant workers in Singapore send part of every paycheck to families back home. That money pays for food, rent, school fees and medical bills, yet the way it travels is stacked against the sender.

- **Hidden costs.** A visible fee plus an exchange-rate margin that workers rarely see.
- **Slow delivery.** Transfers can take hours or days, and cash-out often means travelling to a pickup point.
- **No visibility.** If money is delayed or lost, the sender has little to go on.
- **Hardest on those with least.** A fixed fee takes a bigger share of the small, frequent transfers low-wage workers make.

Every dollar lost to fees is a dollar not spent on a child's school or a parent's medicine.

## Who it is for

| Group | Who |
|---|---|
| Senders | Migrant workers in Singapore: domestic, construction, service and shipyard workers |
| Receivers | Families in the Philippines, including those far from banks |
| Last mile | Licensed remittance outlets, e-wallet providers and community agents |
| Later corridors | Indonesia, India, Bangladesh |

## The solution

Remittance Rail uses stablecoins as the settlement layer, hidden behind a simple app.

1. **Send.** Pay in Singapore dollars through a licensed on-ramp partner. The app shows the exact amount the family will receive before you confirm.
2. **Move.** Value travels as a regulated stablecoin on a low-fee public blockchain. Settlement takes minutes, any day of the week.
3. **Receive.** The family collects local currency in a mobile wallet, or cash at a partner agent, using a one-time code or QR.
4. **Protect.** A smart contract holds the transfer until it is collected. If it is not collected in time, it returns to the sender automatically.
5. **See.** Both sides get a receipt showing amount sent, fee, rate used and amount received, recorded on a public ledger.

The worker only sees a normal app. The blockchain is the plumbing.

## How Web3 adds value

| Pain point today | What Web3 adds |
|---|---|
| Layers of intermediaries raise cost | Direct settlement on a low-fee chain removes middle steps |
| Business-hours settlement | Final settlement in minutes, 24/7 |
| Hidden fees and margins | Fee and rate written into a public receipt anyone can check |
| Money stuck or lost in transit | Programmable escrow with automatic refund |
| Closed agent networks | Any licensed agent can join open rails and compete on price |

## Social impact

- More money reaches families because costs are lower.
- Faster help in medical and disaster emergencies.
- Trust and dignity from a clear record of every transfer.
- Inclusion for receivers without a bank account, through wallets and agents.
- A fairer last mile for local agents and small businesses.

**How we would measure it:** all-in cost of a transfer against the corridor average, time from send to cash-out, share of transfers collected, money saved per user per year, and agents onboarded.

## Business model

A small, transparent per-transfer fee set below the corridor average, plus revenue share from cash-out and on-ramp partners. The target fee will be set after checking current corridor prices, and the pilot tests whether the all-in cost, including on-ramp and off-ramp, still beats the average.

## Pilot plan

| Phase | What | Goal |
|---|---|---|
| 0 | Research and partner conversations: a licensed Singapore money-transfer entity, a stablecoin on/off-ramp, a Philippines cash-out partner | Confirm the legal and operational path |
| 1 | Closed pilot on Singapore to Philippines with a small group of workers and one cash-out partner | Prove cost, speed and collection rate |
| 2 | Add Indonesia, India and Bangladesh and more agents | Scale on the same rails |

## Risks and mitigations

| Risk | Mitigation |
|---|---|
| Licensing for cross-border transfers | Operate through a licensed partner first; seek our own licence later |
| Stablecoin depeg | Regulated, fully reserved stablecoins; convert promptly; cap exposure |
| On/off-ramp costs eat the savings | Negotiate rates, use very low-fee chains, publish the all-in cost |
| KYC and anti-money-laundering | Full identity checks and monitoring through partners |
| Trust among first-time users | Familiar app, agent-assisted onboarding, employer and NGO partnerships |

## Status

This is an idea-stage submission. There is no working prototype yet. Figures that need an external source, such as typical corridor costs and the Singapore licensing position, are marked to verify in the pitch deck and are not stated as fact here.

## Repository

| Path | Contents |
|---|---|
| `pitch/index.html` | 11-slide pitch deck, a single self-contained HTML file |
