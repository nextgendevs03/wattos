# WattOS Portal — Phased Launch: Features, Pricing & Timeline

**Prepared by:** TechPotato Softwares LLP  
**Prepared for:** OSG Oriana India  
**Document Version:** 1.0  
**Date:** January 2026  
**Total Project Cost:** **₹66,28,000 (Sixty-Six Lakh Twenty-Eight Thousand Only)**

---

## 1. Phase Overview

| Phase | Objective | Duration | Amount (INR) | % of total |
|-------|-----------|----------|--------------|------------|
| **Phase 1** | Foundation & core monitoring (*no AI engineer*) | 14–16 weeks | **₹20,12,000** | 30.3% |
| **Phase 2** | Operations (tickets, activities, billing, reports, graphs). *AI engineer starts (data pipeline).* | 14–16 weeks | **₹26,14,400** | 39.4% |
| **Phase 3** | Analytics, HR, AI & experience (workforce, warranties, real-time, AI, integrations, dark mode). *AI engineer (AI service); higher effort for AI integration and integrations.* | 10–12 weeks | **₹20,01,600** | 30.2% |
| **Total** | Full scope (119 screens, all features) | **38–44 weeks** | **₹66,28,000** | 100% |

---

## 2. Phase 1 — Foundation & Core

**Amount:** **₹20,12,000**  
**Duration:** 14–16 weeks  
**Objective:** Production-ready foundation: auth, sites, settings, dashboards, alarms, and basic data pipeline.

### 2.1 Deliverables

- **Auth & RBAC:** Login (username/password), Cognito integration, role-based access, session management.
- **Sites:** Site list, add new site, site detail, map view (basic), filters, export (CSV where applicable).
- **Settings:** Basic site management, user management, permission matrix (site access, roles).
- **Dashboards:** Site overview dashboard (single-site and list), KPIs (power output, energy today, inverter efficiency, DC/AC voltage, grid frequency), basic charts (power generation, efficiency), system health panel.
- **Alarms:** Active alarms list, alarm detail, acknowledge/assign; alarms history with date filters; export to CSV/PDF; basic alarms report.
- **Data pipeline:** Ingestion (MQTT/HTTP or API) for device/site data; validation; 5-minute (and optionally hourly) aggregation; storage in DynamoDB/Timestream; data available for dashboards.
- **Notifications:** Email (SES) for alarm and critical alerts.
- **Print:** Browser print for key screens (list/detail).
- **Infrastructure:** AWS setup (dev + staging), CI/CD pipeline, Aurora PostgreSQL, DynamoDB, S3, CloudFront, API Gateway, Lambda.

### 2.2 Screens (approx)

~30–40 screens (login, site list/detail/map, settings screens, dashboard overview, alarm list/detail/history/report).

### 2.3 Out of scope in Phase 1

Tickets, Work Orders, Activity Log, Billing, Reports, Graphs, Workforce, Warranties, Customers, Components (full), real-time WebSockets, AI analytics, WhatsApp/call, live location, profile modal, dark mode.

---

## 3. Phase 2 — Operations

**Amount:** **₹26,14,400**  
**Duration:** 14–16 weeks  
**Objective:** Full operations: tickets, work orders, activity logging, billing, reports, and graphs.

### 3.1 Deliverables

- **Tickets:** Raise ticket (form, category, priority, attach files), open tickets list, closed tickets list, ticket detail, tickets report (volume, resolution time, SLA).
- **Work Orders:** Active work orders, assigned to me / assigned by me, task detail, work order report.
- **Activity Log:** Maintenance activity log (preventive/corrective), form with checklist, save progress, submit report, add photo, attach document; activity types (cleaning, inverter checks, meter reading, site visit); activity history and report.
- **Billing:** Create bill (line items, tax, energy-based), bill list (draft/sent/paid/overdue), bill detail, update payments (partial, method), billing report; PDF invoice generation.
- **Reports:** ExDR Site Wiz, ExDR Site Inverter Level, ExDR String Level; report generator (date range), report list, report viewer; export options (CSV/PDF).
- **Graphs:** Graph builder (parameters, date range, chart type), defined graphs library, graph viewer; export.
- **Form templates:** Fill form using template where applicable (e.g. activity log).
- **Upload & files:** Upload photo, attach document; download file (reports, exports).
- **Save as draft:** Save progress / save as draft on long forms (e.g. activity log, ticket, bill).

### 3.2 Screens (approx)

~35–45 screens (all tickets, work orders, activity log, billing, reports, graphs screens plus add/edit/view modals).

### 3.3 Out of scope in Phase 2

Workforce (HR), Warranties, Customers, Components (full), real-time analytics (live view), AI analytics, WhatsApp/call, live location, profile modal, dark mode (unless included as stretch).

---

## 4. Phase 3 — Analytics, HR, AI & Experience

**Amount:** **₹20,01,600**  
**Duration:** 10–12 weeks  
**Objective:** Analytics, workforce, warranties, AI, integrations, and UX enhancements.

### 4.1 Deliverables

- **Real-time analytics:** Live view dashboard, live power stream, live site performance, live weather; WebSocket integration for real-time data and live alerts.
- **AI analytics:** AI-powered performance insights and recommendations (Python AI service or Lambda); integration with dashboards and reports.
- **Workforce (HR):** Employee management, attendance & tracking, daily attendance, **live location tracking**, leave management, payroll (view); workforce dashboard.
- **Warranties:** Equipment list, warranty detail, warranty alerts, claim form; document upload.
- **Customers:** Customer list and detail (as per design).
- **Components:** Add new inverter/component (e.g. from global search), component list; integration with sites/settings.
- **Integrations:** WhatsApp (alerts, notifications), voice/call (e.g. Twilio click-to-call).
- **Profile:** Profile action menu; modal for updating user details.
- **Dark mode:** Theme toggle and persistence.
- **Add/edit/view modals:** Complete any remaining add/edit/view modals across modules.
- **Optional:** Additional analytics tools integration (documented per tool).

### 4.2 Screens (approx)

~25–35 screens (analytics, workforce, warranties, customers, components, profile modal, settings refinements).

### 4.3 Milestone

UAT, performance tuning, security review, production deployment, documentation and handover.

---

## 5. Summary Table

| Phase | Amount (INR) | Duration | Cumulative weeks |
|-------|--------------|----------|------------------|
| Phase 1 | ₹20,12,000 | 14–16 weeks | 16 |
| Phase 2 | ₹26,14,400 | 14–16 weeks | 32 |
| Phase 3 | ₹20,01,600 | 10–12 weeks | 42–44 |
| **Total** | **₹66,28,000** | **38–44 weeks** | — |

---

## 6. Payment

- **Full project:** Advance 25% (₹16,57,000) at signing; balance against phase completions (30.3% + 39.4% + 30.2% as Phase 1, 2, 3 complete).

---

*This document is part of the WattOS quotation set. For detailed features and technical architecture, see the Stakeholder Analysis and Technical Documentation.*

**© 2026 TechPotato Softwares LLP. All rights reserved.**
