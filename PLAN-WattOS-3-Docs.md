# WattOS: Three Documents — Plan (Updated)

**Total project cost: ₹66,28,000 (66.28 Lakh)**  
**Year: 2026 | Phase-wise distribution below**

---

## Pricing (Final)

| Item | Amount (INR) |
|------|--------------|
| **Total project cost** | **₹66,28,000** |
| Phase 1 — Foundation & core (30.3%) | ₹20,12,000 |
| Phase 2 — Operations (39.4%) | ₹26,14,400 |
| Phase 3 — Analytics, HR, AI & experience (30.2%) | ₹20,01,600 |
| **Advance (e.g. 25% at signing)** | ₹16,57,000 |

*Excluding GST; AWS paid separately by client. Timeline: 38–44 weeks.*

---

## Inputs

- **SS directory**: [SS](SS/) — **119 files** (WattOS.pdf, WattOS_1–109, login_Screen, Open_search_functionality, Site_sub_Screen1, Profile_menu, Profile_menu_1, alert_notification). **Analyze each screen** to build inventory and feed all three docs.
- **Pricing**: **New** quotation; **do not** align with attached previous docs. **Total = ₹65 Lakh** with phase split above. 30L was prior negotiated price for old scope; scope now increased (110+ screens, full features).
- **Features**: Print, CSV export, form-from-template, upload photo, save/draft, email/WhatsApp/call, download file, real-time analytics/alerts, AI analytics, live location, profile modal, dark mode, WebSockets, add/edit/view modals per screen.

---

## 1. Screen-by-screen analysis (SS) — Mandatory

- Enumerate all 119 files in [SS](SS/).
- **Analyze each screen**: Open each PNG/PDF, infer screen name, module, description, UI patterns (list/detail, form, modal, chart, 3-dot menu, print/export).
- Produce: **Screen inventory table** (file → name, module, description) and **feature checklist per screen**. This drives Doc 1 and Doc 3.

---

## 2. Document 1 — Stakeholder: Features, Screens, APIs, Efforts, Timeline, Price

**Output**: `result/docs/01-Stakeholder-Analysis-Features-Pricing.md`

1. **Executive summary** — Project name, total screens (from SS), total modules, timeline, **total project cost ₹66,28,000**, phase-wise amounts (Phase 1 ₹20,12,000 | Phase 2 ₹26,14,400 | Phase 3 ₹20,01,600).
2. **Screen and feature inventory** — From per-screen SS analysis; table and feature list per module.
3. **API and effort summary** — API count by module; total person-days and weeks.
4. **Pricing** — **Total ₹66,28,000**. Breakdown: Application development, Data engineering, QA. Phase-wise: Phase 1 ₹20,12,000, Phase 2 ₹26,14,400, Phase 3 ₹20,01,600. Advance 25% ₹16,57,000.

---

## 3. Document 2 — Technical: Architecture, Tech Stack (Python/AI), Multi-Language Repo

**Output**: `result/docs/02-Technical-Documentation-Architecture.md`

1. **System overview** — WattOS (cloud, auth, real-time, integrations, AI).
2. **Architecture diagram (Mermaid)** — Client (React, WebSockets), API (Lambda), Auth (Cognito), DB (Aurora, DynamoDB/Timestream), S3, Data pipeline, **AI/ML service (Python)**.
3. **Technology stack** — Frontend (React, TypeScript, Tailwind, Recharts, WebSocket). Backend (Node.js, Lambda). **Python**: data pipeline (Pandas, Airflow or Lambda), **AI/analytics** (FastAPI/Flask; libraries: scikit-learn, LangChain, AWS Bedrock/SageMaker SDK). DB, S3, integrations (SES, WhatsApp, Twilio, maps). Infrastructure (AWS CDK, Docker for Python services).
4. **Multi-language and AI — repository organization (high-level, no folder structure)** — Backend API in Node.js; AI and data pipelines in Python (separate service or Python Lambdas). API contracts (OpenAPI/events) between Node and Python. Python deployed as Lambda or container (ECS/Fargate). How app invokes AI (e.g. API from Node to Python AI service).
5. **Integrations** — Email, WhatsApp, call, location, WebSockets, analytics tools.
6. **Module-wise technical effort** — Table: Module, screens (from SS), backend/frontend/QA days. Include AI/data pipeline.
7. **API inventory** — Estimated endpoints by module.
8. **Security and deployment** — HTTPS, Cognito, RBAC, CI/CD.

---

## 4. Document 3 — Three-phase launch: Features, price per phase, timeline

**Output**: `result/docs/03-Phased-Launch-Pricing-Timeline.md`

1. **Phase overview table** — Phase name, objective, duration, **cost (INR)**, deliverables.
2. **Phase 1** — Foundation & core. **₹22,75,000**. 14–16 weeks. Auth, Sites, Settings, Dashboards, Alarms, data pipeline, email, CSV/print.
3. **Phase 2** — Operations. **₹22,75,000**. 14–16 weeks. Tickets, Tasks, Site Activities, Billing, Reports, Graphs, templates, upload, save/draft, download.
4. **Phase 3** — Analytics, HR, AI & experience. **₹19,50,000**. 10–12 weeks. HR, Warranty, real-time/WebSockets, AI analytics, WhatsApp/call, live location, profile modal, dark mode, modals.
5. **Summary** — **Total ₹66,28,000**. Phase-wise amounts and payment.

---

## 5. PDF/Word export

- **result/docs/README.md** — Instructions to export each .md to PDF/Word (e.g. VS Code “Markdown PDF”, or paste into Google Docs/Word).

---

## 6. Execution order

| Step | Action |
|------|--------|
| 1 | Enumerate all 119 files in [SS](SS/). |
| 2 | Analyze each screen; build screen inventory and feature checklist. |
| 3 | Write **01-Stakeholder-Analysis-Features-Pricing.md** (inventory, features, APIs, efforts, **₹66,28,000 total**, phase amounts). |
| 4 | Write **02-Technical-Documentation-Architecture.md** (architecture, tech stack with Python/AI, multi-language repo high-level, integrations, effort, API). |
| 5 | Write **03-Phased-Launch-Pricing-Timeline.md** (3 phases with **₹20,12,000 | ₹26,14,400 | ₹20,01,600** and timeline). |
| 6 | Add **result/docs/README.md** (PDF/Word export instructions). |
