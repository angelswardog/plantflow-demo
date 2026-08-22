# PlantFlow Production Manager — V9.2 Corrective Test Build

Interactive browser prototype for testing PlantFlow manufacturing operations and workforce-management workflows.

## Demo Accounts

- Production Employee — `EMP1001 / 1111`
- Shipping Employee — `SHIP2001 / 2222`
- Supervisor — `SUP3001 / 3333`
- Manager — `MGR4001 / 4444`
- Office — `OFF5001 / 5555`
- Administrator — `ADM6001 / 6666`

## V9.2 Corrective Fixes

- Live Floor now derives employees and statuses dynamically instead of using the fixed demo roster.
- Off-shift Production employees show no live productivity value.
- Management productivity is calculated from active Direct work instead of hard-coded percentages.
- Supervisor and Manager employee creation/editing now persists across reloads on the same browser/device and newly added employees appear in Live Floor.
- Supervisor Dispatch is restricted to the Supervisor's authorized team.
- Production Complete still starts Indirect immediately, and clock-out is blocked until a required indirect reason is classified.
- Active employees or employees with queued/active work cannot be deactivated until their work/state is resolved.
- Shipping timers are tracked per Shipping employee instead of one global Shipping timer.
- Production management no longer receives Shipping execution authority.
- Office Final Close is restricted to Office/Administrator; Manager/Administrator can reopen a closed record only with a mandatory reason.
- Time Administration is scope-aware and requires correction reasons.
- Shift Handoff and Audit rendering runtime defects were repaired.
- The business date is generated dynamically instead of being hard-coded.
- Built-in QA no longer reports a false all-pass result; unresolved architecture blockers are explicitly reported as failures.

## Test Coverage Before Deployment

The V9.2 corrective build passed **47/47 targeted browser regression checks** across the repaired prototype workflows, including Live Floor, People, employee persistence, Dispatch scope, Time Admin, Production direct/indirect handling, deactivation guards, Shipping discrepancy behavior, Office Final Close, Manager reopen, Handoff and role navigation. These tests validate the static prototype behavior only and do not mean the system is production ready.

## Time Administration Scope

- Supervisor: own direct-report employees
- Manager: employees in the manager's department
- Administrator: active Production and Shipping employees across the organization

Production corrections enforce `Shift Hours = Direct Hours + Indirect Hours`. Shipping corrections enforce `Work Hours <= Shift Hours`. Every correction requires a reason and records the change in the prototype Audit/History data.

## Resetting Test Data

Use **QA Tests → Reset V9.2 Test Data** to clear saved V9.2 browser data and restore the seeded demo state.

## Remaining Architecture Blockers

This remains a browser-test prototype. It intentionally does **not** claim these production capabilities yet:

1. Shared multi-device/server datastore
2. Server-side authentication and RBAC enforcement
3. Immutable server-side audit storage

Data changes persist on the same browser/device using local storage, but they are not shared between separate phones, computers, or browsers. The production implementation still requires a backend/database, secure server authentication, durable transactions, concurrency controls, backups and operational monitoring.
