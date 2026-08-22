# PlantFlow Production Manager — V9.1 Full Master Test

Interactive browser prototype for the PlantFlow manufacturing operations and workforce-management system.

## Demo Accounts

- Production Employee — `EMP1001 / 1111`
- Shipping Employee — `SHIP2001 / 2222`
- Supervisor — `SUP3001 / 3333`
- Manager — `MGR4001 / 4444`
- Office — `OFF5001 / 5555`
- Administrator — `ADM6001 / 6666`

## V9.1 Test Areas

- Production shift, direct/indirect timing and automatic indirect after Production Complete
- Assigned Work and Dispatch
- Shipping Prep, discrepancies and Shipment Ready
- Office Final Close
- Live Floor
- Production Record Control, holds and corrections
- Management Action Center
- People management: add, edit, deactivate/reactivate and employee history
- Organization hierarchy
- Reviews, raise recommendations and approval routing
- Job Master and standard revisions
- Shift Handoff
- Time Administration with scoped supervisor/manager/admin corrections, mandatory reason and audit trail
- Built-in QA screen and Audit Log

## Time Administration Scope

- Supervisor: own direct-report employees
- Manager: employees in the manager's department
- Administrator: active Production and Shipping employees across the organization

Production corrections enforce `Shift Hours = Direct Hours + Indirect Hours`. Shipping corrections enforce `Work Hours <= Shift Hours`. Every time correction records the old values, new values, actor and reason in Audit and employee history.

## Important

This is a browser-test prototype, not a production deployment. A production implementation still requires persistent backend storage, server-side authorization, secure authentication, transactional workflows, immutable audit storage, concurrency controls and production infrastructure.