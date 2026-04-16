# Aha.io Prototype: Product Lifecycle Automation & Governance

**Establishing and Governing Products via AI Agents with MCP Integration**
**Domain: Finance Broker Management & Financial Wealth Management**
**Date: April 2026**

---

## 1. Purpose

This document serves as the operational prototype for using Aha.io as the product lifecycle management system, integrated with AI agents via MCP (Model Context Protocol). It provides:

1. A step-by-step guide for creating a new product workspace from scratch
2. A task list linked to the 28 PM capabilities previously defined
3. Recurring governance automations for ongoing product maintenance
4. An MCP gap analysis identifying what can and cannot be automated
5. A mapping of Aha.io functions to the PM capability model

All activities reference the 7 domains and 28 capabilities from the PM Capability Model document.

---

## 2. Step-by-step guide: Creating a new product

### 2.1 Pre-requisites and information gathering

Before creating a product workspace in Aha.io, the following information must be obtained from the Human Product Leader and Product Specialist panel. This forms the "product intake form" — the minimum viable context an AI agent or human needs to establish the product.

#### Product identity

| Field | Description | Example | Capability |
|:------|:-----------|:--------|:-----------|
| Product name | Official name of the product | "BrokerConnect Platform" | 1.1 |
| Product code | Short reference code for Aha.io | "BCP" | — |
| Product line | Which business line this belongs to | Broker Management | 1.4 |
| Product owner | Named Human Product Specialist | Jane Smith | RASCI |
| Product sponsor | Executive sponsor | VP of Broker Services | 5.1 |

#### Strategic context

| Field | Description | Example | Capability |
|:------|:-----------|:--------|:-----------|
| Product vision | One-sentence vision statement | "The platform brokers trust to manage their entire client lifecycle" | 1.1 |
| Product mission | How the product achieves the vision | "Digitise and streamline broker-client workflows, reducing admin time by 60%" | 1.1 |
| Target market | Primary customer segment | Independent financial brokers, 1–50 advisors | 1.2 |
| Key competitors | Top 3 competitors | CompetitorA, CompetitorB, CompetitorC | 1.2 |
| Revenue model | How the product generates revenue | SaaS subscription, per-seat licensing | 1.3 |
| Pricing tier | Initial pricing strategy | $49/user/month (Growth), $99/user/month (Enterprise) | 1.3 |

#### Initial goals

| Field | Description | Example | Capability |
|:------|:-----------|:--------|:-----------|
| Goal 1 | Primary business objective | Acquire 200 broker firms in first 12 months | 2.3 |
| Goal 2 | Secondary objective | Achieve NPS > 40 within 6 months of launch | 2.3 |
| Goal 3 | Operational objective | Reduce onboarding time to < 2 hours per firm | 2.3 |
| Key metric 1 | Primary success metric | Monthly Recurring Revenue (MRR) | 6.1 |
| Key metric 2 | Engagement metric | Weekly Active Users (WAU) | 6.1 |
| Key metric 3 | Quality metric | Support ticket volume per 100 users | 6.1 |

#### Regulatory context

| Field | Description | Example | Capability |
|:------|:-----------|:--------|:-----------|
| Regulatory jurisdiction | Applicable regulations | FCA (UK), ASIC (Australia) | 7.2 |
| Compliance requirements | Key compliance areas | KYC, AML, data privacy (GDPR) | 7.2 |
| Data classification | Sensitivity level | Confidential — contains PII and financial data | 7.2 |
| Audit requirements | External audit obligations | Annual SOC 2 Type II, FCA regulatory reporting | 7.4 |

### 2.2 Workspace creation sequence

The following steps create the product workspace in Aha.io. Steps marked with **[MCP]** can be automated via the Aha.io MCP server. Steps marked with **[MANUAL]** require human action in the Aha.io UI. Steps marked with **[API]** can be automated via the REST API but are not yet supported by existing MCP tools.

#### Step 1: Create the product workspace [MANUAL]

Aha.io product/workspace creation is an administrative function that requires UI access. This cannot be done via the current MCP server or REST API for security reasons.

- Action: Navigate to Settings → Account → Products → Add Product
- Configure: Product name, product code (prefix), product line assignment
- Assign: Product owner, default team members, permission roles
- Capability link: 1.1 (Product vision & mission), 1.4 (Portfolio management)

#### Step 2: Configure custom fields [MANUAL]

Set up the custom fields that support your capability model.

- Compliance flag (dropdown: Not assessed / Under review / Compliant / Non-compliant) → Capability 7.2
- Regulatory jurisdiction (multi-select: FCA / ASIC / MiFID II / SEC / None) → Capability 7.2
- Data classification (dropdown: Public / Internal / Confidential / Restricted) → Capability 7.2
- PM quality score (number: 0–100) → Capability 7.1
- Customer segment (tags: Broker / Wealth Advisor / Platform Partner) → Capability 3.1
- Automation status (dropdown: Manual / Semi-automated / Fully automated) → Capability 7.1
- Risk level (dropdown: Low / Medium / High / Critical) → Capability 7.3

#### Step 3: Configure workflow statuses [MANUAL]

Define the feature lifecycle workflow that enforces governance.

```
Submitted → Under Review → Approved → In Design → In Development →
QA Testing → UAT → Ready for Release → Released → Retired
```

Required field rules (governance enforcement):
- "Under Review" requires: Description, acceptance criteria, compliance flag
- "Approved" requires: Human Product Leader sign-off (mandatory approval gate)
- "In Development" requires: Assigned engineer, sprint assignment, estimated effort
- "Ready for Release" requires: QA sign-off, compliance flag = "Compliant", release notes
- Capability link: 7.1 (PM standards & process enforcement)

#### Step 4: Create strategic foundation [MCP + API]

These records establish the strategic context. The CPO Agent can create these via MCP/API after receiving the intake form data.

**4a. Create goals** [API — POST /api/v1/products/{product_id}/goals]
- Create Goal 1: Business objective with target metric and timeframe
- Create Goal 2: Customer satisfaction objective
- Create Goal 3: Operational efficiency objective
- Capability link: 2.3 (OKR & goal setting)

**4b. Create initiatives** [API — POST /api/v1/products/{product_id}/initiatives]
- Link each initiative to a parent goal
- Define initiative owner and timeframe
- Capability link: 2.1 (Roadmap management)

**4c. Create first release** [API — POST /api/v1/products/{product_id}/releases]
- Name: "R1 — Foundation Release"
- Set target date, owner, and release theme
- Capability link: 2.2 (Release planning)

**4d. Create knowledge base pages** [MCP — create via pages API]
- Product charter page (vision, mission, target market)
- Competitive landscape page
- Regulatory requirements page
- Decision log page
- Capability link: 6.4 (Documentation & knowledge management)

#### Step 5: Create PRD template and first features [MCP]

**5a. Create PRD template page** [MCP — create_feature or page API]
- Standard PRD template with required sections: problem statement, user stories, acceptance criteria, compliance assessment, success metrics
- Capability link: 4.1 (Requirements & specification), 7.1 (PM standards)

**5b. Create initial features** [MCP — create_feature]
- Create features from the intake form's initial scope
- Assign to Release 1
- Tag with customer segment and compliance flag
- Capability link: 4.1 (Requirements & specification), 4.2 (Backlog management)

#### Step 6: Configure ideas portal [MANUAL]

- Create an ideas portal for broker/advisor feedback intake
- Configure categories aligned to product themes
- Set up voting and status workflows
- Capability link: 6.2 (Customer feedback management)

#### Step 7: Set up integrations [MANUAL]

- Connect Jira/Azure DevOps for engineering workflow sync
- Connect Slack for notifications
- Configure MCP server connection for AI agent access
- Capability link: 5.2 (Cross-functional alignment)

#### Step 8: Establish baseline reports and dashboards [MANUAL + API]

- Product health dashboard (features by status, release progress, goal tracking)
- Governance compliance dashboard (compliance flag distribution, PRD quality scores)
- Feedback dashboard (ideas by category, vote counts, status)
- Capability link: 6.1 (Product analytics & metrics)

---

## 3. Tasks to be done: Setup activities linked to capabilities

Each task is linked to its parent capability and assigned to a role from the RASCI matrix.

### 3.1 One-time setup tasks

#### Domain 1: Product strategy

| Task ID | Task | Capability | Responsible | Automation |
|:-------:|:-----|:-----------|:------------|:-----------|
| S-1.1 | Draft product vision and mission statement | 1.1 | Product Specialist | Manual — human judgment |
| S-1.2 | Create competitive landscape page in Aha.io Knowledge | 1.2 | Research Agent | MCP — create page |
| S-1.3 | Document initial business model and pricing | 1.3 | Product Specialist | Manual — create page via MCP |
| S-1.4 | Register product in portfolio with product line assignment | 1.4 | CPO Agent | Manual — UI only |

#### Domain 2: Product planning

| Task ID | Task | Capability | Responsible | Automation |
|:-------:|:-----|:-----------|:------------|:-----------|
| S-2.1 | Create initial product roadmap with themes and timeframes | 2.1 | CPO Agent | API — create releases + initiatives |
| S-2.2 | Define Release 1 scope with features and target date | 2.2 | Operations Agent | MCP — create_feature per release |
| S-2.3 | Set up OKRs as goals in Aha.io | 2.3 | CPO Agent | API — create goals |
| S-2.4 | Establish team capacity baseline and velocity target | 2.4 | Operations Agent | Manual — requires engineering input |

#### Domain 3: Product discovery

| Task ID | Task | Capability | Responsible | Automation |
|:-------:|:-----|:-----------|:------------|:-----------|
| S-3.1 | Create customer persona pages in Knowledge base | 3.1 | Research Agent | MCP — create page |
| S-3.2 | Document top 5 validated problems from broker interviews | 3.2 | Product Specialist | Manual — human research |
| S-3.3 | Create wireframe/prototype links in feature descriptions | 3.3 | Product Specialist | Manual — creative work |
| S-3.4 | Configure experiment tracking custom fields | 3.4 | Operations Agent | Manual — UI configuration |

#### Domain 4: Product delivery

| Task ID | Task | Capability | Responsible | Automation |
|:-------:|:-----|:-----------|:------------|:-----------|
| S-4.1 | Create PRD template as reusable page template | 4.1 | Governance Agent | MCP — create template page |
| S-4.2 | Populate initial backlog with prioritised features | 4.2 | Governance Agent | MCP — create_feature (batch) |
| S-4.3 | Configure sprint workflow and board views | 4.3 | Product Specialist | Manual — UI configuration |
| S-4.4 | Define QA checklist as required fields on "Ready for Release" | 4.4 | Governance Agent | Manual — workflow configuration |

#### Domain 5: Orchestration & collaboration

| Task ID | Task | Capability | Responsible | Automation |
|:-------:|:-----|:-----------|:------------|:-----------|
| S-5.1 | Create stakeholder map page in Knowledge base | 5.1 | Product Specialist | MCP — create page |
| S-5.2 | Configure notification rules for cross-team visibility | 5.2 | Operations Agent | Manual — UI configuration |
| S-5.3 | Create go-to-market checklist template | 5.3 | Operations Agent | MCP — create page |
| S-5.4 | Document vendor/partner integration requirements | 5.4 | Product Specialist | MCP — create page |

#### Domain 6: Product operations

| Task ID | Task | Capability | Responsible | Automation |
|:-------:|:-----|:-----------|:------------|:-----------|
| S-6.1 | Configure product health dashboard with key metrics | 6.1 | Operations Agent | Manual — dashboard builder |
| S-6.2 | Set up Ideas portal with categories and voting | 6.2 | Operations Agent | Manual — UI configuration |
| S-6.3 | Create competitive intelligence brief template | 6.3 | Research Agent | MCP — create page |
| S-6.4 | Create product documentation structure in Knowledge | 6.4 | Governance Agent | MCP — create pages (batch) |

#### Domain 7: Governance & compliance

| Task ID | Task | Capability | Responsible | Automation |
|:-------:|:-----|:-----------|:------------|:-----------|
| S-7.1 | Configure workflow rules enforcing PM standards | 7.1 | Governance Agent | Manual — workflow configuration |
| S-7.2 | Create regulatory compliance checklist page | 7.2 | Product Specialist | MCP — create page |
| S-7.3 | Create risk register as structured page | 7.3 | Governance Agent | MCP — create page |
| S-7.4 | Verify audit log configuration and retention settings | 7.4 | Governance Agent | Manual — admin settings |

### 3.2 Setup task summary

| Category | Total tasks | MCP automatable | API automatable | Manual only |
|:---------|:----------:|:---------------:|:---------------:|:-----------:|
| Domain 1: Strategy | 4 | 1 | 0 | 3 |
| Domain 2: Planning | 4 | 1 | 2 | 1 |
| Domain 3: Discovery | 4 | 1 | 0 | 3 |
| Domain 4: Delivery | 4 | 2 | 0 | 2 |
| Domain 5: Orchestration | 4 | 3 | 0 | 1 |
| Domain 6: Operations | 4 | 1 | 0 | 3 |
| Domain 7: Governance | 4 | 2 | 0 | 2 |
| **Total** | **28** | **11 (39%)** | **2 (7%)** | **15 (54%)** |

Note: Most "Manual only" tasks are one-time UI configuration (workflow rules, dashboards, portals) that do not recur. The recurring automations below show a much higher automation rate.

---

## 4. Recurring governance automations

These are the routines that must execute on a regular cadence to maintain effective product governance. Each routine is linked to its capability and assigned to an agent or human role.

### 4.1 Daily routines

| Routine ID | Routine | Cadence | Capability | Owner | Automation method |
|:----------:|:--------|:--------|:-----------|:------|:-----------------|
| D-01 | **Backlog hygiene scan** — Identify features without acceptance criteria, compliance flags, or priority scores | Daily | 4.2, 7.1 | Governance Agent | MCP — get_record (scan features), flag incomplete via API update |
| D-02 | **Stale feature alert** — Flag features in "In Development" for > 14 days without status change | Daily | 4.2, 7.1 | Governance Agent | API — query features by status + modified date |
| D-03 | **Blocked feature escalation** — Identify features marked "Blocked" and notify stakeholders | Daily | 4.3, 5.2 | Operations Agent | API — query by status, Slack notification |

### 4.2 Weekly routines

| Routine ID | Routine | Cadence | Capability | Owner | Automation method |
|:----------:|:--------|:--------|:-----------|:------|:-----------------|
| W-01 | **Competitive intelligence brief** — Scan market sources and update competitive landscape page | Weekly | 1.2, 6.3 | Research Agent | Web search + MCP — update page content |
| W-02 | **Feedback synthesis report** — Aggregate and categorise new ideas from Ideas portal, produce weekly summary | Weekly | 6.2 | Operations Agent | API — query ideas by date range, synthesise, create summary page via MCP |
| W-03 | **Release health check** — Report on feature completion rate, scope changes, and risk items for current release | Weekly | 2.2, 6.1 | Operations Agent | API — query features by release + status, generate report |
| W-04 | **PRD quality audit** — Score all new/updated PRDs against template standards | Weekly | 4.1, 7.1 | Governance Agent | MCP — get_record for recent features, evaluate description quality |
| W-05 | **Goal progress update** — Update goal completion percentages based on linked feature status | Weekly | 2.3 | CPO Agent | API — query goals + linked features, calculate progress |
| W-06 | **Risk register review** — Update risk items based on current feature status and blockers | Weekly | 7.3 | Governance Agent | MCP — read risk register page, update with current blockers |

### 4.3 Fortnightly / sprint routines

| Routine ID | Routine | Cadence | Capability | Owner | Automation method |
|:----------:|:--------|:--------|:-----------|:------|:-----------------|
| F-01 | **Sprint retrospective data prep** — Compile velocity, completion rate, and carryover data | Per sprint | 4.3 | Operations Agent | API — query features completed in sprint period |
| F-02 | **Backlog prioritisation refresh** — Re-score backlog items based on updated feedback data and goal progress | Per sprint | 4.2 | CPO Agent | API — query features + ideas data, propose priority changes |
| F-03 | **Capacity vs commitment check** — Compare planned features against team velocity | Per sprint | 2.4 | Operations Agent | API — query release scope vs capacity baseline |

### 4.4 Monthly routines

| Routine ID | Routine | Cadence | Capability | Owner | Automation method |
|:----------:|:--------|:--------|:-----------|:------|:-----------------|
| M-01 | **Roadmap review pack** — Generate roadmap status report for stakeholder review | Monthly | 2.1, 5.1 | CPO Agent | API — query initiatives + releases, compile into summary page via MCP |
| M-02 | **Product health scorecard** — Comprehensive product metrics report (MRR, WAU, NPS, support volume) | Monthly | 6.1 | Operations Agent | External data + MCP — create/update scorecard page |
| M-03 | **Compliance audit report** — Report on compliance flag distribution, non-compliant items, and remediation status | Monthly | 7.2, 7.4 | Governance Agent | API — query features by compliance_flag custom field, generate report |
| M-04 | **PM standards adherence report** — Measure % of features meeting all required fields and quality standards | Monthly | 7.1 | Governance Agent | API — query all features, score against standards checklist |
| M-05 | **Portfolio rebalancing review** — Compare investment allocation across product lines against strategy | Monthly | 1.4 | CPO Agent | API — query features by product line, calculate effort distribution |

### 4.5 Quarterly routines

| Routine ID | Routine | Cadence | Capability | Owner | Automation method |
|:----------:|:--------|:--------|:-----------|:------|:-----------------|
| Q-01 | **OKR review and reset** — Evaluate goal achievement, propose next quarter's OKRs | Quarterly | 2.3 | CPO Agent | API — query goals + progress, draft new OKRs via page creation |
| Q-02 | **Competitive positioning review** — Deep competitive analysis with strategic implications | Quarterly | 1.2 | Research Agent | Web search + MCP — comprehensive landscape update |
| Q-03 | **Product strategy review pack** — Full strategy assessment for Human Product Leader and sponsor | Quarterly | 1.1, 1.3 | CPO Agent | Compile from system data, create strategic review page via MCP |
| Q-04 | **Regulatory compliance deep review** — Comprehensive compliance assessment with remediation plan | Quarterly | 7.2 | Product Specialist + Governance Agent | API query + human review — hybrid |

### 4.6 Recurring automation summary

| Cadence | Total routines | Fully automatable via MCP/API | Hybrid (agent + human) | Manual |
|:--------|:-------------:|:----------------------------:|:---------------------:|:------:|
| Daily | 3 | 3 (100%) | 0 | 0 |
| Weekly | 6 | 5 (83%) | 1 | 0 |
| Per sprint | 3 | 3 (100%) | 0 | 0 |
| Monthly | 5 | 4 (80%) | 1 | 0 |
| Quarterly | 4 | 2 (50%) | 2 | 0 |
| **Total** | **21** | **17 (81%)** | **4 (19%)** | **0** |

---

## 5. MCP gap analysis

### 5.1 Available MCP tools (aha-mcp server)

The primary MCP server (popand/aha-mcp) provides 4 tools:

| MCP Tool | Function | Operations | Capabilities served |
|:---------|:---------|:-----------|:-------------------|
| `get_record` | Retrieve a feature or requirement by reference number | Read | 4.1, 4.2, 4.4, 7.1 |
| `get_page` | Retrieve a knowledge base page by reference number | Read | 6.4, 1.1, 1.2, 7.2 |
| `search_documents` | Search for pages and documents | Read | 6.3, 6.4, 1.2 |
| `create_feature` | Create a new feature in a release | Write | 4.1, 4.2 |

### 5.2 Extended MCP tools (cedricziel/aha-mcp)

The community MCP server adds:

| MCP Tool | Function | Operations | Capabilities served |
|:---------|:---------|:-----------|:-------------------|
| Initiative resources | Read initiative data, comments, epics | Read | 2.1, 1.4 |
| Background sync | Offline database with semantic search | Read | 6.3, 6.4 |
| Vector embeddings | Semantic search across all product data | Read | 3.1, 6.2 |

### 5.3 Available REST API endpoints (not yet in MCP)

These operations are available via the Aha.io REST API but require a custom MCP server extension or direct API calls from agents:

| API Endpoint | Function | Gap impact | Capabilities served |
|:-------------|:---------|:-----------|:-------------------|
| POST /products/{id}/goals | Create goals | High — needed for OKR automation | 2.3 |
| PUT /goals/{id} | Update goal progress | High — needed for goal tracking | 2.3, 6.1 |
| POST /products/{id}/releases | Create releases | High — needed for roadmap automation | 2.1, 2.2 |
| PUT /releases/{id} | Update release details | Medium — needed for release management | 2.2 |
| POST /products/{id}/initiatives | Create initiatives | High — needed for roadmap management | 2.1 |
| GET /products/{id}/features | List all features (filterable) | High — needed for governance scans | 4.2, 7.1, 7.4 |
| PUT /features/{id} | Update feature details | Critical — needed for agent-driven updates | 4.1, 4.2, 7.1 |
| GET /ideas | List ideas from portal | High — needed for feedback synthesis | 6.2 |
| POST /ideas | Create idea records | Medium — needed for competitive gap tracking | 6.2, 6.3 |
| GET /products/{id}/releases/{id}/features | Features per release | High — needed for release health checks | 2.2, 6.1 |
| POST /pages | Create knowledge pages | Available via MCP (partial) | 6.4 |
| PUT /pages/{id} | Update knowledge pages | High — needed for recurring report updates | 6.4, 6.3, 1.2 |

### 5.4 Gap analysis: tasks vs MCP capability

| Task category | Total tasks | Covered by MCP | Covered by API (needs MCP extension) | Not automatable | Coverage % |
|:-------------|:---------:|:-----------:|:------------------------------------:|:---------------:|:----------:|
| Setup tasks | 28 | 11 | 2 | 15 | 46% |
| Daily routines | 3 | 1 | 2 | 0 | 100%* |
| Weekly routines | 6 | 3 | 3 | 0 | 100%* |
| Sprint routines | 3 | 0 | 3 | 0 | 100%* |
| Monthly routines | 5 | 2 | 3 | 0 | 100%* |
| Quarterly routines | 4 | 2 | 1 | 1 | 75%* |

*Asterisk: "Covered" includes API-available operations that require a custom MCP server extension. These are technically automatable but need development work.

### 5.5 Critical MCP gaps to close

| Priority | Gap | Impact | Resolution |
|:--------:|:----|:-------|:-----------|
| 1 | **No feature update (PUT) via MCP** | Cannot update feature status, fields, or compliance flags programmatically. Governance Agent cannot enforce changes. | Extend MCP server with update_feature tool wrapping PUT /features/{id} |
| 2 | **No feature listing/filtering via MCP** | Cannot scan all features for governance checks (missing fields, stale items, compliance gaps). | Extend MCP server with list_features tool wrapping GET /products/{id}/features with filters |
| 3 | **No goal CRUD via MCP** | Cannot create or update OKRs. CPO Agent cannot automate goal management. | Extend MCP server with goal tools wrapping /goals endpoints |
| 4 | **No release CRUD via MCP** | Cannot create releases or update release details. Roadmap automation blocked. | Extend MCP server with release tools wrapping /releases endpoints |
| 5 | **No ideas query via MCP** | Cannot pull feedback data from Ideas portal. Feedback synthesis automation blocked. | Extend MCP server with ideas tools wrapping /ideas endpoints |
| 6 | **No page update via MCP** | Can create pages but cannot update existing ones. Recurring reports must overwrite, not append. | Extend MCP server with update_page tool wrapping PUT /pages/{id} |

### 5.6 Recommended MCP extension development

To achieve the 81% recurring automation target, the following custom MCP tools should be developed as extensions to the existing aha-mcp server:

```
Extended MCP Tools Required:
├── update_feature      — PUT /features/{id} — Priority 1
├── list_features       — GET /products/{id}/features — Priority 1
├── create_goal         — POST /products/{id}/goals — Priority 2
├── update_goal         — PUT /goals/{id} — Priority 2
├── create_release      — POST /products/{id}/releases — Priority 2
├── update_release      — PUT /releases/{id} — Priority 3
├── create_initiative   — POST /products/{id}/initiatives — Priority 3
├── list_ideas          — GET /ideas — Priority 3
├── create_idea         — POST /ideas — Priority 3
└── update_page         — PUT /pages/{id} — Priority 2
```

Estimated development effort: 3–5 days for an experienced Node.js developer familiar with the Aha.io API and MCP protocol.

---

## 6. Aha.io functions mapped to PM capabilities

This mapping ensures every capability in the model has a corresponding Aha.io function and identifies any gaps.

### 6.1 Full capability-to-function mapping

#### Domain 1: Product strategy

| Capability | Aha.io function | Module | Coverage |
|:-----------|:---------------|:-------|:--------:|
| 1.1 Product vision & mission | Strategy → Vision board, Product value canvas | Roadmaps | Full |
| 1.2 Market & competitive analysis | Strategy → Competitors, Knowledge → Pages | Roadmaps + Knowledge | Full |
| 1.3 Business model & pricing | Strategy → Business model canvas, Custom fields | Roadmaps | Full |
| 1.4 Portfolio management | Portfolio → Products view, Portfolio dashboard | Roadmaps | Full |

#### Domain 2: Product planning

| Capability | Aha.io function | Module | Coverage |
|:-----------|:---------------|:-------|:--------:|
| 2.1 Roadmap management | Roadmaps → Visual roadmap, Timeline, Initiatives | Roadmaps | Full |
| 2.2 Release planning | Releases → Release planning, Dependencies, Parking lot | Roadmaps | Full |
| 2.3 OKR & goal setting | Strategy → Goals, Goal progress tracking | Roadmaps | Full |
| 2.4 Capacity & resource planning | Features → Estimates, Team workload views | Develop | Partial — limited native capacity modelling |

#### Domain 3: Product discovery

| Capability | Aha.io function | Module | Coverage |
|:-----------|:---------------|:-------|:--------:|
| 3.1 Customer research & insights | Ideas → Idea portal, Customer interviews | Ideas | Full |
| 3.2 Problem validation | Whiteboards → Concept exploration, Notes | Whiteboards | Partial — no structured validation workflow |
| 3.3 Solution ideation & prototyping | Whiteboards → Wireframes, Concept boards | Whiteboards | Partial — basic wireframing only |
| 3.4 Experimentation & A/B testing | Custom fields + tags for experiment tracking | Custom | Partial — no native experiment framework |

#### Domain 4: Product delivery

| Capability | Aha.io function | Module | Coverage |
|:-----------|:---------------|:-------|:--------:|
| 4.1 Requirements & specification | Features → Description, Requirements, Acceptance criteria | Roadmaps | Full |
| 4.2 Backlog management | Features → List view, Prioritisation, Filters | Roadmaps + Develop | Full |
| 4.3 Sprint collaboration | Develop → Scrum/Kanban boards, Sprint planning | Develop | Full |
| 4.4 Quality assurance oversight | Workflow rules → Required fields, Status gates | Roadmaps | Full |

#### Domain 5: Orchestration & collaboration

| Capability | Aha.io function | Module | Coverage |
|:-----------|:---------------|:-------|:--------:|
| 5.1 Stakeholder management | Roadmaps → Published roadmaps, Presentations | Roadmaps | Partial — no stakeholder CRM |
| 5.2 Cross-functional alignment | Notifications, Integrations (Slack, Teams, Jira) | Platform | Full |
| 5.3 Go-to-market coordination | Features → Launch checklists (via to-dos), Knowledge pages | Roadmaps + Knowledge | Partial — no native GTM workflow |
| 5.4 Vendor & partner management | Knowledge → Partner pages, Custom fields for vendor tracking | Knowledge + Custom | Partial — basic tracking only |

#### Domain 6: Product operations

| Capability | Aha.io function | Module | Coverage |
|:-----------|:---------------|:-------|:--------:|
| 6.1 Product analytics & metrics | Reports → Dashboards, Charts, Pivot tables | Roadmaps | Full |
| 6.2 Customer feedback management | Ideas → Portal, Voting, Categories, Status tracking | Ideas | Full |
| 6.3 Competitive intelligence | Strategy → Competitors, Knowledge → Intelligence pages | Roadmaps + Knowledge | Full |
| 6.4 Documentation & knowledge mgmt | Knowledge → Pages, Templates, Version history | Knowledge | Full |

#### Domain 7: Governance & compliance

| Capability | Aha.io function | Module | Coverage |
|:-----------|:---------------|:-------|:--------:|
| 7.1 PM standards & process enforcement | Workflow rules, Required fields, Status gates, Templates | Platform | Full |
| 7.2 Regulatory compliance oversight | Custom fields (compliance flag, jurisdiction), Knowledge pages | Custom + Knowledge | Full via customisation |
| 7.3 Risk management | Custom fields (risk level), Knowledge pages (risk register) | Custom + Knowledge | Partial — no native risk module |
| 7.4 Audit & traceability | Activity history, Change log, API audit trail | Platform | Full |

### 6.2 Coverage summary

| Coverage level | Count | Capabilities |
|:--------------|:-----:|:------------|
| **Full** | 19 of 28 (68%) | 1.1, 1.2, 1.3, 1.4, 2.1, 2.2, 2.3, 3.1, 4.1, 4.2, 4.3, 4.4, 5.2, 6.1, 6.2, 6.3, 6.4, 7.1, 7.4 |
| **Full via customisation** | 1 of 28 (4%) | 7.2 |
| **Partial** | 8 of 28 (28%) | 2.4, 3.2, 3.3, 3.4, 5.1, 5.3, 5.4, 7.3 |
| **No coverage** | 0 of 28 (0%) | — |

### 6.3 Partial coverage — gap remediation

| Capability | Gap | Remediation |
|:-----------|:----|:-----------|
| 2.4 Capacity planning | No native capacity modelling; relies on estimate fields | Use custom reports combining team size, velocity, and feature estimates. Consider supplementing with external capacity tool. |
| 3.2 Problem validation | No structured validation workflow | Create custom workflow status "Validation" with required evidence fields. Use Knowledge pages for validation reports. |
| 3.3 Solution prototyping | Basic wireframing only in Whiteboards | Accept Aha.io Whiteboards for low-fidelity; use Figma/external tool for high-fidelity and link from features. |
| 3.4 Experimentation | No native experiment framework | Use custom fields (hypothesis, experiment type, success criteria, result) on features tagged "Experiment". |
| 5.1 Stakeholder management | No stakeholder CRM | Use Knowledge pages for stakeholder map; use published roadmaps and presentations for stakeholder communication. |
| 5.3 GTM coordination | No native GTM workflow | Create GTM checklist as a to-do template on release records. Use Knowledge pages for launch plans. |
| 5.4 Vendor management | Basic tracking only | Use Knowledge pages for vendor scorecards. Track integration features with vendor tags. |
| 7.3 Risk management | No native risk module | Create risk register as structured Knowledge page. Use custom fields on features for risk level. Link risk items to features via tags. |

---

## 7. Implementation priority matrix

Based on the analysis above, the following priority sequence is recommended for implementation:

### Phase 1 (Weeks 1–2): Foundation

| Priority | Action | Effort |
|:--------:|:-------|:------:|
| 1 | Create product workspace and configure custom fields | 1 day |
| 2 | Configure workflow statuses and governance rules | 1 day |
| 3 | Create strategic foundation (goals, initiatives, first release) | 0.5 day |
| 4 | Create PRD template and initial feature backlog | 0.5 day |
| 5 | Set up Knowledge base structure | 0.5 day |

### Phase 2 (Weeks 3–4): Agent integration

| Priority | Action | Effort |
|:--------:|:-------|:------:|
| 6 | Deploy aha-mcp server and verify connectivity | 0.5 day |
| 7 | Develop Priority 1 MCP extensions (update_feature, list_features) | 2 days |
| 8 | Configure Governance Agent daily routines (D-01, D-02, D-03) | 1 day |
| 9 | Configure Operations Agent weekly routines (W-02, W-03) | 1 day |

### Phase 3 (Weeks 5–8): Full automation

| Priority | Action | Effort |
|:--------:|:-------|:------:|
| 10 | Develop Priority 2 MCP extensions (goals, releases, update_page) | 2 days |
| 11 | Configure all weekly and monthly routines | 2 days |
| 12 | Set up Ideas portal and feedback synthesis automation | 1 day |
| 13 | Configure CPO Agent quarterly routines | 1 day |
| 14 | Validate end-to-end governance flow with dummy product | 2 days |

**Total estimated effort: 13.5 days**

---

*This document should be read alongside the PM Capability Model & RASCI Matrix, the CPO AI Replacement Feasibility Analysis, and the PM Lifecycle System vs Document Analysis. Together, these four documents form the complete operational blueprint for AI-assisted Product Management governance.*
