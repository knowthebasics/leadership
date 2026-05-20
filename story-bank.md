# Story bank — IC Principal Security (Leadership & influence)

Use these as **structure templates**. Replace names, dates, and numbers with your real outcomes. Each outline follows **Situation → Bet → Coalition → Mechanism → Proof** (one story per interview answer; go deep).

---

## 1. Roadmap / prioritization — “Security backlog vs product velocity”

| Stage | Content |
|--------|---------|
| **Situation** | Product shipping a major release; security had 200+ open findings across severity levels; engineering capacity fixed; leadership asked “what must ship safe?” without slipping the quarter. |
| **Bet** | Prioritize by **exploitability × blast radius × regulatory/customer exposure**, not raw count; explicitly **defer** low-impact items with documented risk acceptance rather than pretending everything is P0. |
| **Coalition** | EM needed bounded scope; PM needed customer-facing narrative; legal needed SOX/data-mapping coverage on specific flows. Aligned on a **single ranked list** published to all three. |
| **Mechanism** | Heatmap tied to product surface + SLA tier; **timeboxed** remediation sprints; exceptions logged with expiry and owner (not permanent waivers). |
| **Proof** | **[YOUR METRICS]** e.g., 100% of Tier-1 findings closed pre-GA; Tier-2 median age reduced from X to Y days; zero Sev-1 auth issues in launch window; explicit deferrals with board-ready risk summary. |

---

## 2. Secure SDLC / developer experience — “Gates that engineers actually use”

| Stage | Content |
|--------|---------|
| **Situation** | Late-stage security reviews blocked releases; developers bypassed process; findings repeated across services (same JWT mistakes, SSRF patterns). |
| **Bet** | **Shift left**: default-secure templates + CI checks over late human gatekeeping; security embedded in **definition of done**, not a separate inspection lane. |
| **Coalition** | Platform eng owned CI; SRE owned rollout safety; security owned rule quality and false-positive budget. Joint SLA: break builds only on **high-confidence** policy violations. |
| **Mechanism** | Org-wide base image / service scaffold; SAST/secret scanning in PR; optional local CLI mirroring CI; office hours for tuning rules; **baseline** then ratchet. |
| **Proof** | **[YOUR METRICS]** e.g., % repos on paved path; PR feedback median time; severe vulns caught pre-merge vs post-deploy; developer NPS or survey delta; reduction in repeat finding classes. |

---

## 3. Incident / crisis — “Customer-visible abuse / data concern”

| Stage | Content |
|--------|---------|
| **Situation** | Spike in account takeover or data exposure symptoms; partial information; exec and comms pressure for immediate answers; engineering chasing logs under load. |
| **Bet** | **Facts-first triage**: contain → scope → communicate known vs unknown; parallel workstreams for technical root cause and customer/regulatory thread without premature blame. |
| **Coalition** | Incident commander (or you're technical lead); legal/comms on messaging; customer support on scripted responses; PM on feature flags / kill switches. |
| **Mechanism** | Runbook for severity gates; war-room agenda; post-incident **system** fixes (detection rule, auth hardening, flag) with owners and dates — not only a narrative report. |
| **Proof** | **[YOUR METRICS]** e.g., time to containment; % affected users bounded; repeat incident prevented (or MTTR down); leadership received daily factual briefs; remediation items closed by deadline. |

---

## 4. Technical debt vs risk — “We can’t fix everything this half”

| Stage | Content |
|--------|---------|
| **Situation** | Legacy service with known crypto or auth debt; new initiative depended on it; security wanted rewrite; product wanted incremental ship. |
| **Bet** | **Compensating controls + timeboxed migration**: short-term hardening (rate limits, WAF rules, segment network) while funding phased replacement; explicit **risk acceptance** for residual gap with expiry. |
| **Coalition** | Finance/architecture council for migration budget; EM for staffing tradeoff; GRC for exception documentation. |
| **Mechanism** | Quarterly review of exceptions; metrics on abuse attempts and error rates; sunset date for legacy path. |
| **Proof** | **[YOUR METRICS]** e.g., no material incident in interim; migration % complete by quarter; exception count trending down; audit trail clean for regulators. |

---

## 5. Cross-functional program — “Security champions / embedded partnership”

| Stage | Content |
|--------|---------|
| **Situation** | Central security team too small for every squad; recurring misconfigurations in one business unit; shadow IT or inconsistent patterns. |
| **Bet** | **Distributed ownership**: train + empower engineers per BU with lightweight charter; central team sets bar and tooling; champions escalate early. |
| **Coalition** | Engineering director sponsored headcount for champions; HR/L&D for training slot; security for curriculum and office hours. |
| **Mechanism** | Champion playbook; monthly sync; shared dashboard per BU; escalation path to threat modeling office hours. |
| **Proof** | **[YOUR METRICS]** e.g., # trained champions; reduction in critical findings per release in pilot BU; faster triage on escalations; BU leads requesting reviews earlier in design. |

---

## 6. Metrics & governance — “Dashboards execs actually use”

| Stage | Content |
|--------|---------|
| **Situation** | Leadership saw security as opaque; endless slide decks; no consistent view of **risk reduction over time**. |
| **Bet** | Few **leading** indicators (coverage, adoption, mean time to remediate by severity) + few **lagging** indicators (incidents, customer trust proxies); reviewed on a fixed cadence. |
| **Coalition** | CFO/risk committee wanted dollarized narrative where possible; CTO wanted engineering friction visible; CISO/legal wanted audit-ready lineage. |
| **Mechanism** | Single source of truth (ASPM / CMDB / ticketing join); exception register with owners and expiry; quarterly “portfolio review” slide — max one page per pillar. |
| **Proof** | **[YOUR METRICS]** e.g., MTTR by severity trend; % critical assets with mandatory controls; exception aging; incident recurrence down YoY. |

---

## 7. M&A / vendor / third-party — “Due diligence at speed”

| Stage | Content |
|--------|---------|
| **Situation** | Acquisition or critical vendor with compressed timeline; incomplete docs; product integration depended on their API and data flows. |
| **Bet** | **Risk-tiered diligence**: deep dive on data custody and auth for highest tiers; lighter questionnaire + spot checks for lower; **integration constraints** (VPC, keys, logging) as non-negotiables. |
| **Coalition** | Corp dev/legal for timeline; integration eng for architecture reality; procurement for contract security schedule. |
| **Mechanism** | Standard diligence packet; technical workshop half-day; remediation conditions precedent or post-close roadmap with board visibility. |
| **Proof** | **[YOUR METRICS]** e.g., all P0 gaps closed or accepted by named exec before cutover; integration tests for authZ paths; no surprise findings in first 90 days post-close. |

---

## 8. Org scaling without direct reports — “Influence at 10x engineering size”

| Stage | Content |
|--------|---------|
| **Situation** | Headcount grew fast; same-size security team; reviews became bottleneck; inconsistent threat modeling depth. |
| **Bet** | **Scale through patterns**: reusable abuse-case library, threat-model templates by archetype (B2B SaaS API, mobile client, batch pipeline), and **office hours** instead of bespoke docs for every team. |
| **Coalition** | Staff+ engineers as reviewers of last resort for novel designs; EM guild agreed on “security ready” checklist for RFCs. |
| **Mechanism** | Internal docs portal; searchable past TM outcomes; automated linking from RFC template to required sections. |
| **Proof** | **[YOUR METRICS]** e.g., TM completion before coding vs after; hours security spent per launch trending down; fewer Sev issues in categories covered by library. |

---

## 9. Disagreement / compromise — “You pushed back and partially lost” (maturity signal)

| Stage | Content |
|--------|---------|
| **Situation** | Product wanted a frictionless onboarding flow; security wanted step-up auth and device binding on high-value accounts; launch date fixed. |
| **Bet** | Argue from **shared constraint** (fraud losses vs conversion); propose **phased** rollout with measurement rather than binary block. |
| **Coalition** | Risk/fraud aligned on loss metrics; PM owned conversion experiment; you owned abuse scenarios and detection backlog. |
| **Mechanism** | Ship minimal step-up on risk score threshold only; A/B test; pre-commit to tighten policy if fraud KPI crosses line; backlog for full binding post-launch. |
| **Proof** | **[YOUR METRICS]** e.g., conversion held within X%; fraud/chargeback reduced in cohort with step-up; documented decision and revisit date — shows you don’t need to “win every battle” to lead. |

---

## 10. Bug bounty / pentest funnel — “Signal, not noise”

| Stage | Content |
|--------|---------|
| **Situation** | High duplicate rate; engineering drowning in low-severity noise; leadership unsure if program improved posture. |
| **Bet** | Treat bounty as **sensor**: tune scope, severity rubric, and triage so findings map to **engineering SLAs** and **root-cause themes** (not ticket volume). |
| **Coalition** | PM for scope; eng managers for capacity; legal for safe harbor and disclosure policy. |
| **Mechanism** | Triage playbook; bucketing into themes; quarterly trend report to leadership; integrate critical classes into SDLC rules. |
| **Proof** | **[YOUR METRICS]** e.g., median $ per valid critical; duplicate rate down; mean time to fix by severity; repeat class “eliminated” via guardrail in CI or design pattern. |

---

## Quick mapping to interview themes

| # | Primary theme |
|---|----------------|
| 1 | Roadmap / prioritization |
| 2 | Secure SDLC / DevEx |
| 3 | Incident / crisis |
| 4 | Technical debt vs risk |
| 5 | Cross-functional program |
| 6 | Metrics & governance |
| 7 | M&A / vendor |
| 8 | Org scaling (no reports) |
| 9 | Disagreement / compromise |
| 10 | Bounty / assessment funnel |

Replace bracketed proof lines with **your** before/after numbers before you practice out loud.
