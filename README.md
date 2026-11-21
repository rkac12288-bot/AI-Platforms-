# Eterna CoE Command

**An enterprise GenAI Centre of Excellence (CoE) platform for a large Brazilian holding company. It tracks adoption, ROI, EBITDA impact, risk and governance across 14 business functions and 6 divisions from one command center.**

Eterna CoE Command is the operating cockpit for a **Hub & Spoke** GenAI programme. A central hub owns the platform, security, standards and shared engineering. Each business function and division is a spoke that owns its use cases, adoption and results. The dashboard helps the CoE Director and the C-suite answer three questions:

1. **Is GenAI creating measurable value?** ROI, EBITDA uplift and cost per interaction.
2. **Where is adoption stalling, and why?** Adoption by function, champion coverage and shadow IT risk.
3. **Is it safe and compliant?** LGPD, BACEN, data isolation and the Brazil AI Bill.

> **Mandate:** deliver **+200–300bps EBITDA** over three years through GenAI across the whole portfolio.

---

## At a glance

| Metric | Current | Target |
|---|---|---|
| Platform maturity | 3.2 / 5 | 4.0 |
| Functions live | 9 / 14 | 14 / 14 |
| Active use cases | 41 (28 in production) | — |
| ROI realised YTD | R$14.2M | R$8.0M |
| EBITDA uplift | +68bps | 200–300bps (3-yr) |
| Cost per AI interaction | R$0.84 | vs R$2.10 shadow IT |
| Shadow IT spend avoided | R$11.2M / yr | — |
| Data incidents / LGPD breaches | 0 | 0 |

*Figures are illustrative demo data.*

---

## Operating model: Hub & Spoke

| | **Hub (central CoE)** | **Spokes (functions & divisions)** |
|---|---|---|
| Owns | Platform, security, data isolation, standards, model contracts | Use cases, adoption, KPIs, business results |
| People | Platform Eng, Data/MLOps, Change Mgmt, Security/CDA, Product/UX squads | AI champion per function, embedded engineers |
| Funding | Master contract with a 40%+ volume discount | Consumption-based chargeback (pay per use) |
| Delivery | **CoE Embed sprints**: 30-day MVPs inside a function | Process redesign and day-to-day use |

**Adoption incentive:** 15% of each function head's bonus is tied to reaching **65% adoption**.

---

## Business functions covered

| Group | Functions |
|---|---|
| Finance & Accounting | Finance, Accounting |
| Ops & Logistics | Operations, Logistics |
| Commercial | Commercial, Marketing, Sales |
| Governance & Control | Legal, Compliance, Controls, Audit Internal |
| People & Strategy | HR, Sustainability, Innovation (Projects) |

Each function has:
- a primary **GenAI use case**, such as SPED fiscal reconciliation, contract risk flagging, OEE prediction or ESG data extraction
- **3 GenAI KPIs**, each with a current value and a target
- adoption %, ROI and EBITDA bps attribution
- a champion status and a **data isolation tier** (MAX / HIGH / MED / LOW)
- the **right interface for its users**: ERP copilot, CRM-embedded assistant, plant-floor voice kiosk, document intelligence UI, and so on

---

## Modules

### Command
- **CoE Command Center:** board summary, insight cards, KPI strip, maturity by pillar, adoption and ROI by function, ROI trajectory, hub capacity, critical actions, embed sprints. Tabs: function heat map, 90-day pilots, OKRs.
- **Business Functions:** one card per function with use case, interface, KPIs, ROI, EBITDA, bonus status, champion and isolation tier. Filterable by group.
- **Capability Radar:** champion coverage, interface type by function, and a policy compliance heatmap (LGPD consent, chargeback, champion, use-case registry, audit trail, data classification).
- **Scenario Planner:** stress-tests budget cuts, champion loss, platform downtime, adoption drop and shadow IT breakouts. Shows the effect on ROI, functions at risk and EBITDA bps.

### Operations
- **Resource Optimizer:** hub squad demand vs capacity, the backlog, and reallocation recommendations.
- **Budget & ROI Tracker:** chargeback statement per function: tokens, tier, charge, shadow IT equivalent, saving and EBITDA.
- **Delivery Health:** RAID log (risks, assumptions, issues, dependencies), blockers, milestones met and delivery confidence.

### Intelligence
- **Enterprise Intelligence:** industry benchmarks, global vs company adoption by function, and the regulatory horizon (BACEN, LGPD/ANPD, Brazil AI Bill PL 2338, CPC/IFRS, CSRD, ANEEL).
- **Decision Engine:** multi-signal escalation. **No escalation fires on a single metric**: at least 2 criteria must breach at the same time. This keeps recommendations defensible to boards, auditors and regulators.
- **Governance Board:** decision register with Hub vs Spoke authority, owner, due date and priority.

### System
- **Initiative Intake:** submission form for new use cases, plus a scored triage backlog.
- **CoE Playbooks:** function onboarding, LGPD and isolation, chargeback calculator, KPI framework, change management, AI governance, ESG AI, EBITDA impact.
- **CoE Policy Settings:** global thresholds (adoption floor, hub utilisation cap, minimum ROI, maturity target, chargeback markup, bonus weight) and data classification per function.

---

## Executive views

A role switcher in the top bar opens a full-screen report written for each executive.

| Role | Focus |
|---|---|
| **CoE Director** | Full platform (default) |
| **CEO** | Portfolio valuation, EBITDA by function, path to the mandate |
| **CDO** | Change management, adoption, exec bonus tracker, shadow IT |
| **CFO** | ROI, chargeback, capital efficiency, unit cost vs shadow IT |
| **CTO** | Infrastructure, RAG pipelines, namespaces, hub capacity, OT integration |
| **CDA** | Data fabric, LGPD, tenant isolation, BACEN pre-audit, PII risk |

---

## Data governance

| Tier | Isolation | Example functions |
|---|---|---|
| **MAX** | Separate vNet, Key Vault, vector store, RBAC namespace and audit shard. Zero shared context. | Finance, Accounting, Audit, Compliance (HR flagged for upgrade) |
| **HIGH** | Separate namespace and audit log | Legal, Controls, Commercial |
| **MED** | Logical partition, shared embedding store, no PII | Operations, Logistics, Sales, Sustainability, Innovation |
| **LOW** | Shared environment, brand content only | Marketing |

All workloads are hosted in **Brazil (Azure Brazil South)** for data residency.

---

## Technical notes

- **Single-file HTML app:** vanilla JavaScript, no build step and no framework.
- **Charts:** [Chart.js 4.4](https://www.chartjs.org/) via cdnjs.
- **Icons:** [Tabler Icons](https://tabler.io/icons) webfont.
- **Data:** a `BUS_FUNCS` model holds all 14 functions. The pages, charts and executive views render from it, so updating one record updates the whole dashboard.
- **Rendering:** each page renders the first time it is opened.
- **Theme:** CSS custom properties (`--vio`, `--tel`, `--grn`, `--amb`, `--red`, `--blu`) with a light background.

### Run it
Open the `.html` file in any modern browser. An internet connection is needed to load Chart.js and the icon font.

### Customise it
- **Functions and KPIs:** edit `BUS_FUNCS` in the `<script>` block.
- **Thresholds:** green is ≥65% adoption, amber is 35–64%, red is below 35%.
- **Tables** (RAID log, governance register, intake, chargeback): each table's data is an array inside its `init…()` function.

---

## Known issues

- Some headline figures don't match the function data. For example, "9 of 14 below 65%" should be 10 of 14, the 44% average adoption is about 52% when calculated, and the function ROIs add up to R$18.0M against the R$14.2M headline.
- The CEO and CFO views sort `BUS_FUNCS` in place, which changes the order in other charts after they are opened. The fix is to sort a copy (`[...BUS_FUNCS].sort(...)`).
- The intake form shows a browser alert and does not save to the backlog.

---

## Related

**Eterna CoE — The Business Case:** an 8-slide board briefing built from this platform's data.
