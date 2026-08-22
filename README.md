# PlantFlow Production Manager — V9.3 Full Regression Build

Interactive browser prototype for PlantFlow.

## Verification
- 142/142 browser regression checks passed before deployment.
- Covers Production Employee, Shipping Employee, Production Supervisor, Shipping Supervisor, Manager, Shipping Manager, Office, and Administrator workflows.
- Includes role/tab navigation, Time Admin, People CRUD, credential reset, Dispatch, Direct/Indirect workflow, Shipping discrepancies, Office close/reopen, Reviews/Raises, Job Master, Handoff, Action Center, persistence and mobile-width checks.

## Demo Accounts
- Production Employee: `EMP1001 / 1111`
- Shipping Employee: `SHIP2001 / 2222`
- Production Supervisor: `SUP3001 / 3333`
- Manager: `MGR4001 / 4444`
- Office: `OFF5001 / 5555`
- Administrator: `ADM6001 / 6666`

## Prototype limitation
This GitHub Pages build persists on the same browser/device. It does not yet provide a shared multi-device database, server-side authentication/RBAC, or immutable server audit storage. Those remain explicit architecture blockers for production.
