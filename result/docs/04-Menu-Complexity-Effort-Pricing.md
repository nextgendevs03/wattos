# WattOS Portal — Menu & Sub-Menu Analysis: Complexity, Effort & Development Pricing

**Prepared by:** TechPotato Softwares LLP  
**Prepared for:** OSG Oriana India  
**Document Version:** 1.0  
**Date:** January 2026  
**Reference:** Screen inventory (SS captures), Stakeholder Analysis, Technical Documentation, Phased Launch  
**Total Project Cost:** **₹66,28,000**

---

## 1. Purpose

This document provides a **screen-level analysis** of the WattOS portal aligned to each **main menu and sub-menu**, derived from the SS (screenshot) captures and existing documentation. For each menu:

- **Screens and sub-menus** are listed with SS file mapping.
- **Complexity** (Low / Medium / High) is assessed per menu.
- **Effort** (person-days: Backend, Frontend, QA) and **development pricing (INR)** are given per menu based on complexity and scope.

Use this for **scope prioritisation**, **phase planning**, and **menu-wise budgeting**.

---

## 2. Complexity Criteria

| Level | Criteria (typical) |
|-------|---------------------|
| **Low** | Simple CRUD, few screens, standard list/detail, no real-time or external integrations. |
| **Medium** | Multiple screens, forms with validation, reports/export, some integrations (e.g. email), moderate APIs. |
| **High** | Real-time/WebSockets, AI/ML, heavy integrations (WhatsApp, call, maps), complex workflows, many entities, data pipeline dependency. |

---

## 3. Menu & Sub-Menu Inventory (from SS)

Mapping of **main menu → sub-menus → screens** and SS file references.

| # | Main Menu | Sub-Menu / Screen | SS / File Reference | Phase |
|---|-----------|-------------------|----------------------|-------|
| 1 | **Login / Auth** | Login (username/password) | login_Screen.pdf | 1 |
| 2 | **Sites** | Sites Overview (list, export, add site, map, filters) | WattOS_1.pdf, Site_sub_Screen1.pdf | 1 |
| | | Site list / map view | Site_sub_Screen1.pdf | 1 |
| | | Site detail, list views | WattOS_3–WattOS_9 | 1 |
| 3 | **Dashboards** | Site Dashboard (single-site: power, energy, efficiency, voltage, frequency) | WattOS.pdf | 1 |
| | | Sites Overview / list dashboards | WattOS_1, WattOS_3–9 | 1 |
| | | KPIs, charts, system health | WattOS.pdf, dashboards | 1 |
| 4 | **Alarms** | Active alarms list | WattOS_11–26 | 1 |
| | | Alarm detail, acknowledge/assign | WattOS_11–26 | 1 |
| | | Alarms history (date filters) | WattOS_11–26 | 1 |
| | | Alarms report, export CSV/PDF | WattOS_11–26 | 1 |
| 5 | **Tickets** | Open tickets list | WattOS_10, WattOS_11–26 | 2 |
| | | Closed tickets list (resolution time, filters) | WattOS_10.pdf | 2 |
| | | Raise ticket (form, category, priority, attach) | WattOS_11–26 | 2 |
| | | Ticket detail | WattOS_11–26 | 2 |
| | | Tickets report (volume, resolution, SLA) | WattOS_11–26 | 2 |
| 6 | **Work Orders** | Active work orders | WattOS_28–49 | 2 |
| | | Assigned to me / Assigned by me | WattOS_28–49 | 2 |
| | | Task detail | WattOS_28–49 | 2 |
| | | Work order report | WattOS_28–49 | 2 |
| 7 | **Activity Log (Site Activities)** | Maintenance activity log (form, checklist, save progress, submit) | WattOS_27.pdf | 2 |
| | | Add photo, attach document; activity types | WattOS_28–49 | 2 |
| | | Activity history and report | WattOS_28–49 | 2 |
| 8 | **Billing** | Create bill (line items, tax, energy-based) | WattOS_28–49 | 2 |
| | | Bill list (draft/sent/paid/overdue) | WattOS_28–49 | 2 |
| | | Bill detail, update payments (partial, method) | WattOS_28–49 | 2 |
| | | Billing report; PDF invoice | WattOS_28–49 | 2 |
| 9 | **Reports** | ExDR Site Wiz, ExDR Site Inverter Level, ExDR String Level | WattOS_51–63 | 2 |
| | | Report generator (date range), report list, viewer | WattOS_51–63, WattOS_65–91 | 2 |
| | | Export (CSV/PDF) | WattOS_51–63 | 2 |
| 10 | **Graphs** | Graphs Dashboard (Power/Energy/Performance/Weather/Financial/Comparative) | WattOS_50.pdf | 2 |
| | | Graph builder (parameters, date range, chart type) | WattOS_51–63 | 2 |
| | | Defined graphs library, graph viewer, export | WattOS_51–63 | 2 |
| 11 | **Analytics** | Real-Time Analytics (live view, live power stream, live site performance, weather) | WattOS_64.pdf | 3 |
| | | Live alerts, WebSocket integration | WattOS_64–91 | 3 |
| | | AI analytics (performance insights, recommendations) | WattOS_65–91 | 3 |
| 12 | **Workforce (HR)** | Workforce Dashboard | WattOS_92.pdf | 3 |
| | | Employee Management, Attendance, Daily attendance | WattOS_93–109 | 3 |
| | | Live location tracking | WattOS_92–109 | 3 |
| | | Leave management, Payroll (view) | WattOS_93–109 | 3 |
| 13 | **Warranties** | Equipment list, warranty detail, warranty alerts | WattOS_93–109 | 3 |
| | | Claim form, document upload | WattOS_93–109 | 3 |
| 14 | **Customers** | Customer list and detail (as per design) | WattOS_93–109 | 3 |
| 15 | **Components** | Add new inverter/component (e.g. global search), component list | WattOS_65–91, Open_search | 3 |
| 16 | **Settings** | Site management, user management, permission matrix | WattOS_65–91, WattOS_93–109 | 1, 2, 3 |
| | | DC capacity, sites, components, users, permissions | WattOS_65–91 | 1–3 |
| 17 | **Shared / Global** | Global search (Dashboard, Alarms, Tickets, Work Orders; type-ahead) | Open_search_functionality.pdf | 2–3 |
| | | Profile action menu; modal for user details | Profile_menu.PNG, Profile_menu_1.PNG | 3 |
| | | Alerts / Notifications UI | alert_notification.PNG | 1–3 |

---

## 4. Complexity by Menu

| Main Menu | Complexity | Rationale |
|-----------|------------|-----------|
| **Login / Auth** | Medium | Cognito, RBAC, session management, multi-tenant identity. |
| **Sites** | Medium | List, map, filters, export, add/detail; multiple views. |
| **Dashboards** | High | KPIs, charts, real-time data, data pipeline dependency, system health. |
| **Alarms** | High | Active/history/report, acknowledge/assign, export, email notifications, pipeline-driven. |
| **Tickets** | Medium | Raise/open/closed, SLA, report, file attach; no real-time/AI. |
| **Work Orders** | Medium | Active/assigned, task detail, report; workflow. |
| **Activity Log** | High | Long forms, checklist, templates, save draft, photo/document upload, activity types, report. |
| **Billing** | High | Create bill, line items, tax, energy-based logic, payments, PDF invoice, report. |
| **Reports** | Medium | ExDR (Site/Inverter/String), generator, date range, export. |
| **Graphs** | Medium | Graph builder, multiple chart types, date range, export; time-series data. |
| **Analytics** | High | Real-time (WebSocket), live view, AI analytics service, Python integration. |
| **Workforce (HR)** | High | Attendance, live location, leave, payroll; maps/location API. |
| **Warranties** | Medium | Equipment list, warranty detail, alerts, claim form, document upload. |
| **Customers** | Low | List and detail (as per design); standard CRUD. |
| **Components** | Medium | Add component (e.g. global search), list, link to sites/settings. |
| **Settings** | High | Sites, users, permissions, DC capacity; RBAC, multi-tenant. |
| **Shared / Global** | Medium | Global search, profile modal, alerts; used across modules. |

---

## 5. Effort & Development Pricing by Menu

Effort (person-days) is from **Technical Documentation — Module-Wise Technical Effort**.  
**Pricing** = (Module total person-days ÷ 760) × ₹66,28,000 (rounded to nearest ₹1,000).

| # | Main Menu | Screens (approx) | Backend (days) | Frontend (days) | QA (days) | **Total (days)** | **Development price (INR)** | Phase |
|---|-----------|------------------|----------------|-----------------|-----------|------------------|----------------------------|-------|
| 1 | Auth & RBAC | 2 | 14 | 10 | 5 | **29** | **₹2,53,000** | 1 |
| 2 | Sites | 4 | 10 | 12 | 5 | **27** | **₹2,36,000** | 1 |
| 3 | Dashboards | 4 | 16 | 22 | 8 | **46** | **₹4,01,000** | 1 |
| 4 | Alarms | 5 | 16 | 18 | 7 | **41** | **₹3,57,000** | 1 |
| 5 | Tickets | 6 | 18 | 20 | 8 | **46** | **₹4,01,000** | 2 |
| 6 | Work Orders | 5 | 14 | 16 | 6 | **36** | **₹3,14,000** | 2 |
| 7 | Activity Log | 8 | 22 | 24 | 10 | **56** | **₹4,88,000** | 2 |
| 8 | Billing | 6 | 22 | 18 | 8 | **48** | **₹4,18,000** | 2 |
| 9 | Reports | 5 | 18 | 14 | 6 | **38** | **₹3,31,000** | 2 |
| 10 | Graphs | 4 | 16 | 18 | 6 | **40** | **₹3,49,000** | 2 |
| 11 | Analytics (real-time + AI) | 4 | 24 | 18 | 8 | **50** | **₹4,36,000** | 3 |
| 12 | Workforce (HR) | 5 | 16 | 16 | 6 | **38** | **₹3,31,000** | 3 |
| 13 | Warranties | 4 | 12 | 12 | 5 | **29** | **₹2,53,000** | 3 |
| 14 | Customers | 2 | 6 | 8 | 3 | **17** | **₹1,48,000** | 3 |
| 15 | Components | 3 | 10 | 10 | 4 | **24** | **₹2,09,000** | 3 |
| 16 | Settings | 7 | 20 | 22 | 8 | **50** | **₹4,36,000** | 1–3 |
| — | Data pipeline (Python) | — | 40 | — | 8 | **48** | **₹4,18,000** | 1–2 |
| — | AI service (Python) | — | 20 | — | 5 | **25** | **₹2,18,000** | 3 |
| — | Infrastructure & DevOps | — | 22 | — | 6 | **28** | **₹2,44,000** | 1 |
| — | Integration & E2E testing | — | 12 | 14 | 16 | **42** | **₹3,67,000** | 2–3 |
| | **Total** | **~70+** | **~370** | **~260** | **~130** | **760** | **₹66,28,000** | — |

*Data pipeline and AI service support multiple menus (e.g. Dashboards, Alarms, Analytics); cost is shared across phases.*

---

## 6. Summary by Complexity

| Complexity | Menus | Total person-days (menu-only*) | Total price (INR) (menu-only*) |
|------------|-------|---------------------------------|--------------------------------|
| **High** | Dashboards, Alarms, Activity Log, Billing, Analytics, Workforce, Settings | ~309 | ~₹26,92,000 |
| **Medium** | Auth, Sites, Tickets, Work Orders, Reports, Graphs, Warranties, Components, Shared | ~337 | ~₹29,35,000 |
| **Low** | Customers | 17 | ~₹1,48,000 |

*Excluding Data pipeline, AI service, Infrastructure, Integration & E2E.*

---

## 7. Summary by Phase

| Phase | Menus (main) | Menu-level effort (days) | Phase amount (INR) |
|-------|----------------|---------------------------|---------------------|
| **Phase 1** | Auth, Sites, Dashboards, Alarms, Settings (partial), Data pipeline (partial), Infra | ~248 | ₹20,12,000 |
| **Phase 2** | Tickets, Work Orders, Activity Log, Billing, Reports, Graphs, Settings (partial), Data pipeline, Integration | ~310 | ₹26,14,400 |
| **Phase 3** | Analytics, Workforce, Warranties, Customers, Components, Settings (refinements), AI service, Shared (profile, dark mode), Integration | ~202 | ₹20,01,600 |

---

## 8. How to Use This Document

- **Prioritisation:** Use complexity and price per menu to decide order of build or MVP vs later phases.
- **Budgeting:** Use “Development price (INR)” per menu for menu-wise budget allocation.
- **Scope change:** If a menu is dropped or simplified, adjust effort and recalc price using (days ÷ 760) × ₹66,28,000.
- **New scope:** Estimate new screens/sub-menus, assign complexity, and derive effort and price using the same rates and total project days.

---

*This document is part of the WattOS quotation set. For features and APIs see Stakeholder Analysis; for architecture and tech stack see Technical Documentation; for phased amounts and timeline see Phased Launch.*

**© 2026 TechPotato Softwares LLP. All rights reserved.**
