# PlantFlow Production Manager — V9.5.1 Integrity Patch

Interactive browser prototype for PlantFlow manufacturing operations, workforce workflows, employee performance and Operations Analytics.

## V9.5.1 Integrity repairs
- Dated Production and Shipping time sessions; Today no longer carries prior-day counters.
- Time Admin is date-specific and Production Direct corrections reconcile to a job allocation.
- People mutations revalidate department/reporting scope inside the mutation handler.
- Shipping Employee actions enforce active prep ownership.
- On-Time Delivery includes all due work in the denominator and compares normalized timestamps.
- Stale tabs block mutations before in-memory/UI state changes.
- Scheduled pay-effective audit events are attributed to SYSTEM.
- Planned Quantity and Job Standard reject zero/invalid values explicitly.
- Team standings require a minimum production sample; Quality King requires meaningful volume.
- Required Indirect reason selector has an accessible name.
- Browser state is tamper-evident for authorization, credential state and compensation integrity; persisted credentials use proof values rather than plaintext PINs.

## Verification
- 360/360 fresh functional, hostile-state, regression and stress assertions passed before deployment.
- 1,451 visible enabled button appearances traversed across all 11 seeded roles/accounts with no unwired action.
- Exact release SHA-256: `8ea9e505eafa7fa0e4fd58637ef886b6d5d4733638e01aa6a7da9565e9369c64`

## Prototype boundary
This remains a GitHub Pages browser prototype. True shared state, confidential credential/compensation storage, authoritative server-side authentication/RBAC and immutable audit require the production backend. Client tamper-evidence is defense-in-depth, not a substitute for server security.
