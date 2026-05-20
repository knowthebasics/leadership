# Security strategy one-pager (generic IC Principal narrative)

Use this in **open-ended strategy** questions (“How would you stand up / evolve security here?”). Speak for 2–3 minutes using this skeleton, then add **one concrete mechanism** per pillar (CI rule, ritual, dashboard).

---

## North star (one sentence)

**Ship fast with justified risk:** increase customer trust and operational resilience while keeping product and engineering velocity predictable — security is measured by **outcomes and adoption**, not activity.

---

## Pillars (3–4) and portfolio bets

### Pillar A — Secure SDLC and paved roads

- **Multi-quarter bets**: default-secure templates; high-confidence checks in CI/CD; threat modeling tied to RFC/architecture reviews for high-risk changes.
- **Explicitly not funding** (example): bespoke manual review for every low-risk CRUD service without scaling champions first.

### Pillar B — Identity, data, and trust boundaries

- **Bets**: consistent authZ patterns for APIs; data classification and minimum necessary access; secrets and key management standards tied to rotation and blast-radius limits.
- **Not funding**: one-off encryption projects without asset inventory or ownership mapping.

### Pillar C — Detection, response, and resilience

- **Bets**: telemetry parity for critical paths; actionable alerts with owners; game days / chaos for dependency failures; incident metrics that drive **system** fixes.
- **Not funding**: expanding tool footprint without tuning and runbook coverage.

### Pillar D — Governance, measurement, and executive rhythm

- **Bets**: small set of leading + lagging KPIs; exception process with owners, expiry, and quarterly review; portfolio review slide (one page per pillar) for leadership.
- **Not funding**: governance theater (policies nobody operationalizes).

---

## Metrics

| Type | Examples |
|------|-----------|
| **Leading** | % critical services on paved path; PR-time security signal resolution; threat models completed before coding for Tier-1 launches; mean time to first security review in design. |
| **Lagging** | Incidents by severity and recurrence; MTTR by severity; customer-facing abuse/fraud proxies; audit/regulatory findings closed on time. |
| **Health of program** | Exception aging and count trending down; duplicate finding classes eliminated via guardrails; developer friction surveys / NPS where available. |

Pick **3–4 metrics** max for exec-facing narrative; tie each to a pillar.

---

## Review cadence

- **Monthly**: engineering-facing — backlog burn, rule noise, CI breakage budget.
- **Quarterly**: leadership — pillar progress, explicit cuts/deferrals, risk acceptance summary, replan triggers (major incident, M&A, new regulator).
- **Replan triggers**: Sev-1 cluster in one domain; new product surface (AI features, market expansion); material architecture pivot.

---

## Closing line for exec prompts

**Problem → Options → Recommendation → Ask:**  
“We’re constrained on X; options are A (faster, residual risk Y), B (slower, cleaner). I recommend B for these two revenue-critical flows and A elsewhere with compensating controls. I need [risk acceptance / headcount / platform priority] by [date].”

---

## Company overlay (clone per target employer)

Duplicate this block into a new file, e.g. `strategy-overlay-<company>.md`, and fill before each loop.

### Employer

- **Company name**:  
- **Primary product / attack surface** (consumer, B2B, regulated vertical):  
- **Known public posture** (breaches, bug bounty, compliance marketing — factual only):  

### Threat and regulatory context

- **Top 3 plausible adversaries or abuse cases** for *their* product:  
- **Regulatory or contractual pressure** (GDPR, HIPAA, SOC2, PCI, FedRAMP, etc.):  

### Engineering culture fit

- **How security should meet them** (e.g., heavy internal platform vs startup scrum):  
- **One concrete mechanism** you’d emphasize first here (and why):  

### North star tweak (optional one-line rewrite)

- **Company-specific north star** (still outcome-focused, not tool-focused):  

### Pillars — local emphasis

| Pillar | Emphasize / de-emphasize here because… |
|--------|------------------------------------------|
| A — SDLC | |
| B — Identity/data | |
| C — Detection/resilience | |
| D — Governance | |

### Proof you’d cite in conversation

- **Two alignment phrases** that show you did homework (product names, segments, or recent public initiatives):  

---

## Practice checklist

- [ ] Deliver north star + pillars in under 90 seconds cold.  
- [ ] Name one **mechanism** per pillar without slides.  
- [ ] State what you **won’t** do this year and why.  
- [ ] End with **one ask** if the interviewer plays exec.  
