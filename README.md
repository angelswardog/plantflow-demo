# PlantFlow Production Manager — V9 Demo

Interactive manufacturing workflow test build for PlantFlow.

## Demo Accounts

- Production Employee — `EMP1001 / 1111`
- Shipping Employee — `SHIP2001 / 2222`
- Supervisor — `SUP3001 / 3333`
- Manager — `MGR4001 / 4444`
- Office — `OFF5001 / 5555`
- Administrator — `ADM6001 / 6666`

## Test Flow

1. Sign in as Production Employee.
2. Clock into shift.
3. Start an assigned job.
4. Enter Good Pieces and Scrap.
5. Complete Production.
6. Confirm PlantFlow automatically enters `INDIRECT — REASON REQUIRED`.
7. Sign in as Shipping Employee and move Production Complete work through Shipping Prep to Shipment Ready.
8. Sign in as Office and perform Verify & Final Close.
9. Test Supervisor/Manager/Admin views for Live Floor, Dispatch, People, and Audit.

This repository is the browser-test prototype. The production build will use persistent backend storage, server-side authorization, secure authentication, concurrency controls, immutable audit records, and the complete PlantFlow product specification.
