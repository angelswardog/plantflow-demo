# PlantFlow Production Manager — V9.4 Integrity / Hardening Build

Interactive browser prototype for PlantFlow.

## V9.4 hardening

- Timestamp-derived Production and Shipping time recovery
- Active-work guards for role/department changes and deactivation
- Mutation-level Dispatch scope/job validation
- Dispatch reprioritize, hold/release and cancel controls
- Shipment Ready invalidation after Production quantity/scrap edits
- Atomic Shipping-state cleanup when records return to Production
- Shipping handoff/release workflow
- Time Admin indirect-block reconciliation
- Review performance/reliability persistence and returned-review resubmission
- Supervisor team scorecard review snapshot
- Office personnel review support for Administrator
- Compensation redaction in Supervisor History/Audit
- Cross-department Audit scoping
- Reactivation clears prior lockout state
- Same-browser multi-tab stale-state warning/protection

## Test evidence

The exact release candidate passed 98/98 full regression checks, 44/44 edge/button/mobile checks, 63/63 adversarial authorization/state checks, and 26/26 V9.4 hardening checks. JavaScript syntax, unique DOM IDs and invalid nested controls were also verified.

## Important architecture boundary

This remains a static browser prototype. Shared multi-device state, server authentication/RBAC, immutable audit storage, database transactions/concurrency, backups and production observability require the backend/database implementation.
