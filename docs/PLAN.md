# Plan

Remittance Rail is an idea-stage project. This plan describes how it would move from idea to a working pilot. Nothing here is built yet, and nothing is presented as measured data.

## Goal

Make sending money home cheaper, faster and visible for migrant workers in Singapore, starting with the Singapore to Philippines corridor.

## Principles

- **Start with one corridor.** Prove it end to end before adding more.
- **Use licensed partners first.** Cross-border transfers are regulated, so we operate through licensed entities before seeking our own licence.
- **Hide the blockchain from users.** Workers use a normal app. Stablecoins and smart contracts are the plumbing.
- **Measure honestly.** Publish the all-in cost, including on-ramp and off-ramp fees, and compare it with the corridor average.

## Phases

### Phase 0: Research and partners
- Talk to a licensed Singapore money-transfer entity, a stablecoin on and off-ramp provider, and a Philippines cash-out partner.
- Confirm the legal and operational path, including KYC and anti-money-laundering duties.
- Collect verified corridor data (typical cost, speed, main cash-out channels) from public sources such as World Bank remittance price data and central bank publications.
- Interview workers, employers and NGOs to validate the problem and the app flow.

**Exit criteria:** at least one licensed on-ramp partner and one cash-out partner agree to a pilot, and the legal path is confirmed in writing.

### Phase 1: Closed pilot (Singapore to Philippines)
- Build the minimum product described in [HOW_TO_BUILD.md](HOW_TO_BUILD.md).
- Run a small, invited group of workers with one cash-out partner.
- Measure cost, speed and collection rate for every transfer.

**Exit criteria:** the measured all-in cost beats the corridor average, transfers settle and are collected reliably, and users say they would keep using it.

### Phase 2: Scale on the same rails
- Add more cash-out agents and wallets in the Philippines.
- Add Indonesia, India and Bangladesh as new corridors.
- Move from one verifier or operator to a wider set of partners.

## Success metrics

| Metric | What it tells us |
|---|---|
| All-in cost versus corridor average | Whether workers actually keep more of their money |
| Send-to-cash-out time | Whether the speed promise holds |
| Share of transfers collected successfully | Whether the last mile works |
| Money saved per user per year | The impact on a family |
| Agents onboarded | Whether the network can grow |

## Milestones

1. Partner conversations started and documented.
2. Legal path confirmed with a licensed partner.
3. Escrow contract written and tested.
4. Sender and receiver flows working end to end on a test network.
5. Closed pilot launched with real partners.
6. Pilot results published, including the all-in cost.
7. Second corridor started.

## Team and roles needed

- Product and operations lead, to run partner conversations and the pilot.
- Smart contract and backend engineer.
- Mobile or web app engineer.
- Compliance advisor, to guide licensing, KYC and anti-money-laundering.
- Community partner, such as an employer group or NGO, to reach first users.

## Open questions

- Which licensed Singapore entity and which on-ramp will partner for the pilot?
- Which Philippines cash-out channel fits first: mobile wallet, agent cash pickup, or both?
- What collection timeout is fair for families that may be far from an agent?
- What is the target fee, once real on-ramp and off-ramp costs are known?
