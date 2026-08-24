# PlantFlow Production Manager — V9.5 Analytics & Team Performance

Interactive browser prototype for PlantFlow manufacturing operations and workforce management.

## V9.5 additions
- Employee **My Performance** dashboard with production, quality, Direct/Indirect time, adjusted utilization, trends, job history, and “Where Did My Shift Go?” breakdown.
- Employee **Team Production Board** visible to employees with normalized friendly competition, quality-weighted scoring, privacy protections, range filters, team targets and achievements. Productivity above 100% provides no extra leaderboard score.
- Supervisor **Team Performance** and Manager/Admin **Operations Analytics** dashboards.
- KPI monitoring for Output, Downtime, Schedule Attainment, On-Time Delivery, Quality and Operational Loss with drilldowns.
- Dispatch now records Planned Quantity and Due Date so schedule/delivery KPIs are based on actual workflow data.
- Operational delay categories distinguish machine/material/quality losses from employee-controlled performance.

## Verification
V9.5 passed a fresh 396-check browser QA/regression sweep before deployment, covering all 11 demo accounts, role/tab/mobile navigation, new analytics and privacy behavior, Production → Shipping → Office, Time Admin, People, Dispatch, Reviews, Job Master, visible-control wiring, and live dashboard refresh.

## Prototype boundary
This GitHub Pages build still uses same-browser/device state. A production deployment requires a shared database, server-side authentication/RBAC, immutable server audit storage, backups, observability and real multi-user concurrency.
