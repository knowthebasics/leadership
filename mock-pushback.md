# Mock VP pushback — top 4 stories from story bank

Pair this with [story-bank.md](story-bank.md) stories **1–4**. For each pushback, answer in **one sentence** out loud, then expand only if the interviewer probes.

**Practice loop:** Record yourself; aim for calm pace; avoid defending ego — defend **tradeoffs and outcomes**.

---

## Story 1 — Roadmap / prioritization (“Security backlog vs product velocity”)

| Skeptical VP pushback | One-line rebuttal |
|------------------------|-------------------|
| “You’re just hiding risk by deferring findings.” | “Deferrals were **named, time-bound, and tied to compensating controls or acceptance by the risk owner** — not silent backlog decay.” |
| “Why should I trust your severity ranking over Engineering’s?” | “We used **shared criteria** — exploitability, blast radius, and regulatory exposure — and published the ranked list so EM and PM could challenge specifics, not philosophy.” |
| “Product slipped anyway — security was the bottleneck.” | “We **bounded** security scope to Tier-1 surfaces pre-GA and moved Tier-2 into SLA-backed sprints so the slip wasn’t unbounded discovery work.” |
| “Sounds like paperwork — what actually got safer?” | “**Before/after:** Tier-1 issues at zero at launch; repeat vulnerability classes dropped because we stopped chasing noise at the wrong phase.” |
| “What if we’d been wrong about what was Tier-1?” | “We tied tiers to **architecture and data flow** reviews with EM sign-off, and we had a **fast escalation** path when telemetry or incidents contradicted the map.” |

---

## Story 2 — Secure SDLC / developer experience (“Gates engineers actually use”)

| Skeptical VP pushback | One-line rebuttal |
|------------------------|-------------------|
| “CI security checks slow teams down — we can’t afford it.” | “We shipped **high-confidence rules first**, measured **median PR feedback time**, and burned down false positives with a **budget** — friction went to teams that were skipping basics, not everyone.” |
| “Developers will always hate security.” | “They hate **unpredictable** security; we gave **local parity** with CI, fast exemptions with owners, and **office hours** — adoption became the metric.” |
| “This is tool theater — scanners don’t stop real attackers.” | “Scanners **eliminate entire bug classes** at scale; we paired them with **design-time** patterns for auth and trust boundaries where scanners are blind.” |
| “Who owns when the pipeline breaks?” | “Joint ownership: **platform** for stability, **security** for rule quality and rollback criteria — we didn’t security-break builds without an on-call path.” |
| “How do you know you didn’t just shift burden to SRE?” | “We tracked **rollback rate, flake rate, and override counts** by rule; noisy rules got disabled or tuned — that’s how we kept social license.” |

---

## Story 3 — Incident / crisis (“Customer-visible abuse / data concern”)

| Skeptical VP pushback | One-line rebuttal |
|------------------------|-------------------|
| “Why didn’t you communicate faster externally?” | “We separated **known facts from hypotheses**; comms went out when **scope and containment** were defensible — faster wrong messaging would’ve destroyed trust.” |
| “Are you sure it wasn’t just noise?” | “We used **severity gates** and correlation across signals; we assumed breach until disproved for **customer-data paths** — that’s standard for principal judgment.” |
| “Someone needs to be held accountable now.” | “Accountability is **post-learning**; during response I optimized for **scope control and customer impact**, not blame — we assigned owners for fixes with dates.” |
| “This will never happen again, right?” | “We committed to **specific system changes** — detection, auth hardening, flags — with metrics; ‘never again’ without mechanisms is theater.” |
| “Security should own the whole incident.” | “I owned **technical integrity and risk narrative**; IC structure followed company command model — I integrated legal/comms/engineering so we didn’t compete in public.” |

---

## Story 4 — Technical debt vs risk (“Can’t fix everything this half”)

| Skeptical VP pushback | One-line rebuttal |
|------------------------|-------------------|
| “You’re asking me to accept insecure architecture.” | “I’m asking for **time-bound acceptance of residual risk** with **compensating controls** and a funded migration — that’s how adults ship with legacy.” |
| “Compensating controls are just duct tape.” | “They’re **instrumented** duct tape: rate limits, segmentation, and monitoring with **exit criteria** tied to the real replacement work.” |
| “Why didn’t you escalate harder earlier?” | “I escalated when **blast radius and exploitability** crossed our threshold; earlier escalation without options would’ve burned credibility — I brought **options**, not panic.” |
| “Engineering will never pay the migration tax.” | “We tied migration to **customer incidents and audit debt** with dates; exceptions **expire** so the tax isn’t infinite deferral.” |
| “Sounds like you compromised too much.” | “Principals **optimize for business survivability**: we shipped with bounded exposure, measurable monitoring, and a **single accountable exec** for the residual risk.” |

---

## Out-loud drill (10 minutes)

1. Pick **one** story. Deliver **Situation + Bet** in 45 seconds.  
2. VP interrupts: pick a random row from that story’s table — answer **only** the one-liner.  
3. Repeat for **Coalition + Mechanism** in 60 seconds; another random pushback.  
4. Close with **Proof** using your real metrics (fill in from story-bank).  

Do this **twice weekly** until answers feel automatic, not memorized.
