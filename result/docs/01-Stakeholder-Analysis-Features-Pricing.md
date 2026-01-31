# WattOS Portal — Stakeholder Analysis: Features, Screens, APIs, Efforts, Timeline & Pricing

**Prepared by:** TechPotato Softwares LLP  
**Prepared for:** OSG Oriana India  
**Document Version:** 1.0  
**Date:** January 2026  
**Total Project Cost:** **₹66,28,000 (Sixty-Six Lakh Twenty-Eight Thousand Only)**  
**Year:** 2026

---

## 1. Executive Summary

This document provides a complete analysis of the **WattOS** platform — a cloud-based **Solar Assets Performance Monitoring Suite** — for client stakeholders. The platform enables comprehensive monitoring of solar installations including real-time dashboards, alarm management, ticketing, work orders, activity logging, billing, reporting, HR (workforce), warranty tracking, analytics, and AI-powered insights.

| Item | Value |
|------|--------|
| **Total Project Cost** | **₹66,28,000** |
| **Phase 1 (Foundation & Core)** | ₹20,12,000 (30.3%) |
| **Phase 2 (Operations)** | ₹26,14,400 (39.4%) |
| **Phase 3 (Analytics, HR, AI & Experience)** | ₹20,01,600 (30.2%) |
| **Advance (25% at signing)** | ₹16,57,000 |
| **Timeline to Production** | 38–44 weeks |
| **Total Screens (captured)** | 119 screens |
| **Total Modules** | 12+ major modules |

*Excluding GST. AWS infrastructure paid separately by client.*

---

## 2. Screen and Feature Inventory

### 3.1 Screen Inventory (from SS captures)

Screens were captured from the live WattOS Figma prototype. Total **119 screen captures** in the SS directory.

| File(s) | Screen / Module | Description |
|---------|----------------|-------------|
| login_Screen.pdf | Login | Authentication: username/password |
| WattOS.pdf | Site Dashboard | Single-site view: power output, energy today, inverter efficiency, DC/AC voltage, grid frequency |
| WattOS_1.pdf | Sites Overview | List of sites, export, add new site, map view, filters |
| Site_sub_Screen1.pdf | Sites (sub) | Sites list / map view |
| WattOS_3–WattOS_9 | Sites / Dashboards | Site details, list views, dashboards |
| WattOS_10.pdf | Closed Tickets | Closed tickets list, resolution time, filters |
| WattOS_11–WattOS_26 | Tickets, Alarms | Open/closed tickets, raise ticket, alarm list, alarm detail, history, reports |
| WattOS_27.pdf | Maintenance Activity Log | Site Activities: activity form, save progress, submit report, add photo, attach document, checklist |
| WattOS_28–WattOS_49 | Site Activities, Work Orders, Billing | Activity logs, work orders, billing list, create bill, payments |
| WattOS_50.pdf | Graphs Dashboard | Power/Energy/Performance/Weather/Financial/Comparative graphs, custom graph builder |
| WattOS_51–WattOS_63 | Graphs, Reports | Graph builder, report generator, ExDR (Site/Inverter/String level), export |
| WattOS_64.pdf | Real-Time Analytics | Live performance, live view, live alerts, live power stream, live site performance, weather |
| WattOS_65–WattOS_91 | Analytics, Reports, Settings | Analytics dashboards, reports, settings (sites, components, users, permissions) |
| WattOS_92.pdf | Workforce Dashboard | HR: Employee Management, Attendance, Live Location Tracking, Leave, Payroll; Warranties |
| WattOS_93–WattOS_109 | Workforce, Warranties, Customers, Components, Settings | HR sub-screens, warranty management, customers, components, user/permission settings |
| Open_search_functionality.pdf | Global Search | Quick access: Dashboard, Alarms, Tickets, Work Orders; type-ahead search |
| Profile_menu.PNG, Profile_menu_1.PNG | Profile / User Menu | Profile action menu; modal for updating user details |
| alert_notification.PNG | Alerts / Notifications | Real-time alerts, notification UI |

### 3.2 Feature List (by category)

**Cross-cutting (many screens)**  
- Print (opens browser print / print window)  
- Export to CSV  
- Form fill using template  
- Upload photo / Attach document  
- Save progress / Save as draft  
- Download file  
- 3-dot action menu per screen  
- Add / Edit / View modals per screen  

**Integrations**  
- Direct email (SES)  
- WhatsApp integration  
- Call integration (e.g. Twilio)  
- Live location tracking (Workforce)  

**Real-time & analytics**  
- Real-time analytics (live view, live power stream, live site performance)  
- Real-time alerts (WebSocket-based)  
- AI integration for analytics (performance insights, recommendations)  

**UX**  
- Dark mode  
- Profile action menu → modal for updating details  
- Global search (Open_search_functionality)  
- WebSocket integration for live data  

### 3.3 Module-wise feature summary

| Module | Purpose | Key features | Screens (approx) |
|--------|---------|--------------|-----------------|
| **Auth** | Login, RBAC | Username/password, session | 1+ |
| **Dashboards** | Real-time monitoring | KPIs, charts, site comparison, AI insights | 3+ |
| **Sites** | Site management | List, map, filters, export, add site | 3+ |
| **Alarms** | Alarm management | Active, history, report, export CSV/PDF | 4+ |
| **Tickets** | Issue tracking | Raise, open, closed, report, SLA | 5+ |
| **Work Orders** | Task/work order tracking | Active, assigned, completion | 4+ |
| **Activity Log** | Maintenance logging | Log entry, save progress, templates, upload photo | 6+ |
| **Billing** | Invoicing & payments | Create bill, list, payments, report, PDF | 5+ |
| **Graphs** | Custom visualizations | Graph builder, defined graphs, export | 3+ |
| **Reports** | ExDR & reporting | Site/Inverter/String level, export, date range | 4+ |
| **Analytics** | Real-time & AI analytics | Live view, live alerts, AI insights | 3+ |
| **Workforce (HR)** | HR functions | Attendance, live location, leave, payroll | 4+ |
| **Warranties** | Warranty tracking | Equipment list, warranty detail, claims | 3+ |
| **Customers** | Customer management | List, detail (as per design) | 2+ |
| **Components** | Component management | Add inverter/component, list (e.g. Open_search Add New Inverter) | 2+ |
| **Settings** | Administration | Sites, users, permissions, DC capacity | 6+ |
| **Shared** | Profile, search, alerts | Profile modal, global search, alert notification | 3+ |

---

## 4. API and Effort Summary

### 4.1 API inventory (estimated)

| Module | Endpoints (approx) | Methods (approx) |
|--------|---------------------|------------------|
| Auth | 5 | 10 |
| Sites | 8 | 16 |
| Dashboards | 10 | 20 |
| Alarms | 12 | 24 |
| Tickets | 10 | 20 |
| Work Orders / Tasks | 8 | 16 |
| Site Activities | 14 | 28 |
| Billing | 10 | 20 |
| Reports | 8 | 16 |
| Graphs | 6 | 12 |
| Analytics (incl. AI) | 8 | 16 |
| Workforce (HR) | 10 | 20 |
| Warranties | 6 | 12 |
| Customers | 4 | 8 |
| Components | 5 | 10 |
| Settings | 12 | 24 |
| **Total** | **~134** | **~268** |

*Includes APIs for export CSV, print, file upload, templates, save draft, notifications, WhatsApp/call, location, and AI analytics.*

### 3.2 Effort summary

| Category | Person-days (approx) | Person-weeks (approx) |
|----------|----------------------|------------------------|
| Backend development | 280 | 56 |
| Frontend development | 260 | 52 |
| Data engineering & pipelines | 50 | 10 |
| QA & testing | 110 | 22 |
| **Total effort** | **~700** | **~140** |

*Timeline: 38–44 weeks with a team of 5 resources (1 Architect, 1 AI engineer from Phase 2, 2 Full-stack developers, 1 QA).*

---

## 5. Pricing

### 5.1 Total project cost

| Component | Amount (INR) |
|-----------|--------------|
| **Total project cost** | **₹66,28,000** |
| — Application development (incl. Architect, Full-stack) | ₹49,36,000 |
| — Data engineering & AI (AI engineer, Phase 2 & 3) | ₹7,56,000 |
| — Quality assurance (QA) | ₹9,36,000 |

*Excluding GST. AWS paid separately by client.*

### 5.2 Phase-wise distribution

| Phase | Scope | Amount (INR) | % of total |
|-------|--------|--------------|------------|
| **Phase 1** | Foundation & core (Auth, Sites, Settings, Dashboards, Alarms, data pipeline, email, CSV/print). *No AI engineer.* | **₹20,12,000** | 30.3% |
| **Phase 2** | Operations (Tickets, Work Orders, Activity Log, Billing, Reports, Graphs, templates, upload, save/draft, download). *AI engineer starts (data pipeline).* | **₹26,14,400** | 39.4% |
| **Phase 3** | Analytics, HR, AI & experience (Workforce, Warranties, real-time/WebSockets, AI analytics, WhatsApp/call, live location, profile modal, dark mode, modals). *AI engineer (AI service); higher effort for AI integration and integrations.* | **₹20,01,600** | 30.2% |
| **Total** | Full scope (119 screens, all features) | **₹66,28,000** | 100% |

### 5.3 Payment schedule (example)

| Milestone | % | Amount (INR) | Trigger |
|-----------|---|--------------|---------|
| Advance | 25% | ₹16,57,000 | Contract signing |
| M1: Phase 1 complete | 30.3% | ₹20,12,000 | Foundation & core delivered |
| M2: Phase 2 complete | 39.4% | ₹26,14,400 | Operations delivered |
| M3: Phase 3 complete | 30.2% | ₹20,01,600 | Analytics, HR, AI & experience delivered |
| **Total** | **100%** | **₹66,28,000** | — |

*Actual payment terms to be agreed in contract (e.g. advance then phase-wise against deliverables).*

### 5.4 Cost justification (man-days & per-hour rates)

The total project cost is derived from **760 person-days** of effort and the following **team composition and rates** (8 hours per day):

| Role | Count | Rate (₹/hr) | Cost per person-day (8 hr) | Person-days | Total cost (INR) |
|------|-------|-------------|----------------------------|-------------|------------------|
| **Architect** (incl. DevOps) | 1 | 2,000 | 16,000 | 50 | 8,00,000 |
| **AI engineer** | 1 | 1,500 | 12,000 | 63 | 7,56,000 |
| **Full-stack developer** | 2 | 1,000 | 8,000 | 517 (combined) | 41,36,000 |
| **QA engineer** | 1 | 900 | 7,200 | 130 | 9,36,000 |
| **Total** | **5** | — | — | **760** | **66,28,000** |

*Note: AI engineer is engaged from **Phase 2** only (data pipeline in Phase 2, AI analytics service in Phase 3). Phase 3 includes additional AI and full-stack effort for AI integration, real-time analytics, and external integrations.*

**Phase-wise cost breakdown (same rates):**

| Phase | Architect | AI engineer | Full-stack | QA | Phase total (INR) |
|-------|-----------|-------------|------------|-----|-------------------|
| Phase 1 | 20 days | 0 days | 180 days | 35 days | **20,12,000** |
| Phase 2 | 15 days | 20 days | 220 days | 52 days | **26,14,400** |
| Phase 3 | 15 days | 43 days | 117 days | 43 days | **20,01,600** |
| **Total** | **50** | **63** | **517** | **130** | **66,28,000** |

---

## 6. Timeline (indicative)

| Phase | Duration | Cumulative |
|-------|----------|------------|
| Phase 1 — Foundation & core | 14–16 weeks | Week 16 |
| Phase 2 — Operations | 14–16 weeks | Week 32 |
| Phase 3 — Analytics, HR, AI & experience | 10–12 weeks | Week 42–44 |
| **Total** | **38–44 weeks** | — |

---

*This document is part of the WattOS quotation set. For technical architecture and phased launch details, see the Technical Documentation and Phased Launch documents.*

**© 2026 TechPotato Softwares LLP. All rights reserved.**
