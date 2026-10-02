# Replit Build Specification — OribiServ ITOM

Build a production-ready full-stack IT Operations Management (ITOM) web application from the accompanying Excel template kit.

## Source workbook

ITOM_ITSM_Excel_Template_Kit_OribiServ.xlsx

## Product goal

Turn the workbook's operational registers and dashboards into a browser-based ITOM platform for OribiServ. Preserve the workbook concepts while replacing spreadsheets with relational data, forms, filters, workflows, dashboards and audit history.

## Recommended stack

- Frontend: React + TypeScript + Tailwind CSS
- Backend: Node.js + TypeScript API
- Database: PostgreSQL using Drizzle ORM
- Charts: Recharts
- Authentication: email/password with secure sessions
- Deployment: Replit
- Export: XLSX and CSV exports

## Core navigation

1. Command Center
2. Service Desk
3. Incidents
4. Problems
5. Changes
6. Releases
7. SLA / OLA
8. Monitoring & Events
9. Assets / CMDB
10. Network / Servers / Applications
11. Backup & DR
12. Vendors / Contracts
13. Risk / Controls / Audit
14. Finance / Costs / ROI
15. Capacity / Performance
16. Automation / Runbooks / SOP
17. Knowledge Base
18. Planning / On-Call / Handover
19. Reports
20. Administration

## Dashboard requirements

### ITOM Command Center
Show:
- Open incidents
- P1/P2 incidents
- SLA breaches
- SLA compliance %
- Service availability %
- Failed backup jobs
- Changes awaiting approval
- Overdue problems
- Critical risks
- Assets due for renewal
- Vendor contracts due for renewal
- Monthly IT operating cost
- Automation hours saved

Include trend charts for incidents, SLA compliance, availability, cost and changes.

### Service Desk
Ticket queue with status, priority, category, assignee, requester, SLA deadline, age, resolution time and customer satisfaction. Include queue metrics, ticket aging and first-contact-resolution.

### Incidents
Full incident lifecycle:
New -> Assigned -> Investigating -> Pending -> Resolved -> Closed.
Support severity, impact, urgency, priority, assignment group, communications, SLA timer, resolution and linked problem/change.

### Problems
Known-error database, root-cause analysis, 5-Whys, corrective actions, linked incidents, ownership and lifecycle.

### Change Management
Normal, standard and emergency changes. Include risk score, impact assessment, implementation plan, rollback plan, CAB workflow, approvals, scheduled window, conflicts and post-implementation review.

### SLA / OLA
Service-level register with response and resolution targets, actuals, SLA status, breach reason and monthly compliance.

### Monitoring
Event/alert ingestion-ready data model with severity, source, CI, timestamp, acknowledgement, escalation and remediation. Include monitoring coverage and remediation tracking.

### Asset / CMDB
CI register with CI type, owner, location, lifecycle, status, serial/asset number, warranty, relationships and dependencies. Support applications, servers, network devices, software licences and cloud assets.

### Backup / DR
Backup jobs, job status, retention, repository, last successful backup, restore tests, RTO/RPO, recovery priority and DR exercises.

### Vendors
Vendor register, contracts, renewal dates, owner, service, spend, performance, risk and issues.

### Governance
Risk register, controls, control testing, audit actions, policies and compliance tracking.

### Finance
ZAR currency by default. Include budget, actual, forecast, variance, cloud spend, service costing, cost allocation, ROI and payback period.

### Capacity / Performance
Track resources, utilization, baseline, forecast, growth, capacity thresholds, demand and capacity gaps.

### Automation / Runbooks / SOP
Track automation opportunities, estimated savings, implementation status, runbooks, SOPs, owners, review dates and continual-improvement actions.

### Planning
Operations planner, maintenance calendar, Gantt-style work plan, RACI, on-call rota and shift handover.

## Database entities

Create normalized tables for:
users, teams, services, service_requests, incidents, incident_updates, problems, known_errors, rca_analyses, changes, change_approvals, cab_meetings, releases, slas, ola_targets, sla_measurements, monitoring_events, alerts, assets, configuration_items, ci_relationships, network_devices, servers, applications, software_licenses, backup_jobs, restore_tests, dr_plans, dr_exercises, vendors, vendor_contracts, vendor_issues, risks, controls, control_tests, audits, policies, costs, cloud_costs, service_costs, roi_cases, capacity_records, performance_baselines, demand_forecasts, storage_records, automations, runbooks, sops, knowledge_articles, improvement_actions, maintenance_tasks, on_call_shifts, handovers, raci_entries, audit_log.

## Common platform features

- Global search
- Saved filters
- Pagination
- Sorting
- CSV/XLSX export
- Print-friendly reports
- Role-based access
- Audit log for create/update/delete/approve/close operations
- Attachments metadata
- Comments/activity timeline
- Linked records
- Bulk import from the workbook
- Bulk export to workbook
- Responsive desktop-first UI
- Dark mode
- Empty states
- Error handling
- Form validation
- Toast notifications

## Roles

Admin, IT Manager, Service Desk Agent, IT Operations Engineer, Network Engineer, Systems Engineer, Security/Risk, Finance, Auditor, Read Only.

## Import requirement

Provide an admin workflow:
Upload Excel -> inspect sheets -> map columns -> validate rows -> preview -> import.

Allow re-import without duplicating records when a stable external ID is present.

## Reports

- Daily Operations Report
- Weekly IT Operations Review
- Monthly ITOM Review
- Service Desk Performance
- SLA Compliance
- Incident Trend
- Problem Review
- Change Calendar
- Asset Lifecycle
- Backup/DR Readiness
- Vendor Performance
- Risk & Controls
- IT Cost Review
- Capacity Review
- Continual Improvement

## UI direction

Use a professional enterprise operations-center aesthetic:
- Dense but readable data tables
- KPI cards
- Left navigation
- Filter bars
- Status badges
- Drill-down modals/drawers
- Timeline activity
- Clear severity/priority indicators
- Accessible contrast
- Keyboard-friendly forms

Brand the interface as:
OribiServ ITOM
Subtitle: IT Operations Management Command Center

## Deliverables

Generate:
- Complete Replit application
- PostgreSQL schema and migrations
- Seed/demo data matching the workbook domains
- All routes and forms
- Dashboards
- Import/export tooling
- README with setup instructions
- .env.example
- Automated tests for key calculations and API routes

Do not create placeholder pages. Every navigation item must have a functional screen backed by database records or a useful empty-state workflow.
