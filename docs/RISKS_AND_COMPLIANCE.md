# Risks and Compliance

An honest list of what could go wrong and how we plan to handle it. This is not legal advice. The legal path must be confirmed with a licensed partner and qualified advisors in Phase 0.

## Regulation and licensing

Cross-border money transfer is regulated in Singapore and in receiving countries.

- **Plan:** operate through a licensed partner first, then pursue our own licence as we grow.
- **To confirm:** the exact licensing requirements and which entity holds them, using official guidance from the relevant authorities.
- **Rule for us:** do not move real customer money until the legal path is confirmed in writing.

## Identity checks and anti-money-laundering

- Full identity verification for senders, and screening and monitoring, through a licensed partner or compliance provider.
- Transfer limits and monitoring for unusual patterns.
- A clear process for reporting and for freezing suspicious activity as the law requires.

## Stablecoin risk

- **Depeg or issuer failure.** Use regulated, fully reserved stablecoins, hold value in them only briefly, convert promptly, and cap exposure.
- **Freeze or blacklist risk.** Understand the issuer's policies and avoid designs that depend on funds sitting idle.

## Cost risk

The savings can disappear if on-ramp and off-ramp costs are high.

- Negotiate partner rates and pick a very low-fee chain.
- Measure and publish the all-in cost for every transfer.
- If the all-in cost does not beat the corridor average, say so and change the model rather than hide it.

## Smart contract risk

- Bugs could lock or lose funds.
- **Mitigation:** thorough tests including invariant and fuzz tests, minimal contract logic, an independent audit before real funds, and a limit on funds at risk during the pilot.

## Privacy

A public ledger is transparent, but workers and families should not be exposed.

- Use pseudonymous transfer ids.
- Keep names, phone numbers and identity data off-chain.
- Publish only what a receipt needs: amount, fee, rate and status.

## Operational risk

- **Collection failures.** If a family cannot reach an agent in time, the transfer would be refunded. Choose a fair timeout and offer a way to extend it.
- **Partner failure.** Avoid depending on a single partner over time. Plan for backup cash-out options.
- **Support.** Workers need help in their own language, quickly, especially if money seems delayed.

## Adoption risk

- First-time users may distrust a new service. Address it with familiar design, community and employer partners, and agent-assisted first transfers.
- Low digital confidence. Keep the flow simple and offer assisted onboarding.

## Summary table

| Risk | Main response |
|---|---|
| Licensing | Licensed partner first, confirm in Phase 0 |
| KYC and AML | Licensed compliance provider and monitoring |
| Stablecoin depeg | Regulated coins, brief holding, exposure caps |
| Ramp costs | Negotiate, low-fee chain, publish all-in cost |
| Contract bugs | Tests, audit, funds-at-risk limit |
| Privacy | Pseudonymous ids, data off-chain |
| Adoption | Community partners, assisted onboarding |
