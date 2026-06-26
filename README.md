# My AI Product Strategy
> A living strategy built across 6 sessions. Each module adds one component.
> By Module 6, this repo IS your strategy — version-controlled, board-ready, portable.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)
**What we're building, for whom, why now.**

- **Product:** Agent Trainer — a realistic AI simulation platform that gives contact center agents a risk-free environment to practice voice and chat interactions before they take a real call. Set Context. Simulate. Evaluate.
- **AI Value Archetype:** Copilot — augments agent skill, scales with seats
- **Vulnerability Scores:** Moat 4/5 · Data 5/5 · Platform 4/5
- **Top Risk:** Genesys or NICE ships native agent simulation — customers don't need a separate license because training is already inside the platform they use daily
- **Confidence:** M
- **Prototype:** [link]
- **Kill Criteria:** A tier-1 contact center platform (Genesys, NICE, Five9) ships native agent simulation with multilingual support — and two enterprise customers delay renewal to evaluate it

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)
**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** 15/20
- **Weakest Loop:** Network Loop (2/5) — each new customer starts from zero, no cross-org signal flows back to improve the platform. Blocked by data policy.
- **Competitive Position:** Strong contextual moat through 20+ languages and accent simulation, proprietary 5-skill scoring framework, and 50+ customer configurations that take months to rebuild. Data advantage through PII compliance and proprietary evaluation data. Platform exposure is the active risk — Genesys (named attacker) and ElevenLabs (voice layer owner) are 12–18 months from shipping competitive features.
- **Encroachment Defense:** Multilingual voice depth Genesys won't match at launch. Consulting layer (BA onboarding + CSM) embeds us in customer workflow. Horizon 2 LMS/CRM integrations turn platform attackers into distribution partners before they become competitors.
- **Vendor Portability:** Partial — dual dependency on Anthropic (Claude) for simulation and evaluation, ElevenLabs for voice and accents. Abstraction layer and fallback providers not yet in place.

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)
**Will this make money or bleed it?**

- **Gross Margin (current):** 35–55% on recurring — ElevenLabs voice and CSM cost compress margin on small accounts and heavy users
- **Gross Margin (AI-adjusted):** Target 55–70% post cascading strategy (Haiku/Sonnet routing) and hybrid pricing implementation
- **Pricing Model:** Hybrid — base seat fee (per license) + usage tier above session threshold. Pure seat-based pricing absorbs ElevenLabs cost spikes from power users.
- **Cascading Strategy:** Claude Haiku for simple grading tasks → Claude Sonnet for full customer persona simulation and nuanced skill evaluation. Expected ratio: 30% Haiku / 70% Sonnet.
- **Break-even at:** License price must clear $60–70/agent/month given $29–46 COGS (Claude + ElevenLabs + CSM). $15,000 onboarding fee is margin-positive and funds BA cost.

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)
**Why users will trust a probabilistic system.**

- **Reliability Target:** >95% accuracy · <1% hallucination rate · <3 sec p95 latency · <3% drift velocity
- **Golden Dataset:** 5 rows, 3 adversarial — covering split skill scores, PII detection, escalation realism, language consistency, and confident-but-wrong agent responses
- **Confidence UX:** Tiered — >90% scores display immediately; 70–90% flagged for review; <70% withheld from agent until trainer/manager approves
- **HITL Architecture:** Confidence <70% → customer's own trainer/manager reviews before score released. PII detected → session quarantined. Score dispute → trainer override within 48 hours. Drift alert → product team audit. CSM does not override scores.
- **Failure Mode Coverage:** Confident-but-wrong answers scored incorrectly by LLM judge (biggest gap — needs factual grounding layer); PII in agent responses; language switching mid-session; AI customer breaking character; boundary scores (2–3/5) where LLM judge is least reliable

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)
**What breaks when this scales — and what compounds.**

- **Compounding System:** Three loops — Skill Score Correction (active, but overrides not systematically fed back); Scenario Difficulty (broken — failure data exists but requires manual BA intervention, fix: automated gap alerts at >40% failure rate); Cross-Customer Benchmark (missing — blocked by no cross-org data sharing policy)
- **Governance Posture:** No PII in simulations. No cross-org data sharing. Scores require trainer/manager approval below 70% confidence. Simulation Agent operates in-context only. Evaluation Agent cannot be overridden by CSM. Weekly automated eval cadence, monthly human review, quarterly full policy audit.
- **Shadow AI Status:** 4 tools found — 3 build candidates (native scenario generation, in-platform analytics, multilingual scenario translation), 1 partner (LMS/CRM integration via Zapier). Estimated hidden spend: $200–600/month per customer.
- **Agent Boundaries:** Simulation Agent — in scenario context only, no external communications, no real customer data access. Evaluation Agent — autonomous above 70% confidence, requires trainer/manager approval below threshold, cannot share data across orgs.
- **Regulatory Exposure:** EU AI Act (limited risk — human always in evaluation loop). GDPR/CCPA (contact centers handle sensitive data — no PII policy enforced). SOC 2 (required for enterprise buyers).

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)
**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now — 0–3 months):** Automate scenario gap alerts from failure patterns. Launch in-platform score dispute mechanism (trainer/manager only). Ship session usage dashboard to eliminate manual Sheets exports.
- **Horizon 2 (Next — 3–9 months):** Native scenario generation from transcript — remove ChatGPT workaround. LMS and CRM integrations (Salesforce, Genesys, NICE) — turn attackers into distribution. In-platform analytics and reporting — deepen switching cost.
- **Horizon 3 (Bet — 9–18 months):** Vertical scenario libraries by industry (insurance, banking, telecom, healthcare). Adaptive simulation difficulty based on agent skill history. Industry-recognized agent simulation certification.
- **Board Narrative:** Agent Trainer is the only AI simulation platform purpose-built for contact centers, combining multilingual voice emulation with proprietary skill evaluation to cut agent ramp time before they ever take a real call.
- **Key Metrics:** Agent ramp time reduction per customer · License renewal rate · Onboarding-to-active ratio · Session volume per agent per month

→ Details: [`06-the-pitch/`](06-the-pitch/)- **Governance Posture:** AI customer simulation and AI evaluation scoring across all voice and chat simulation sessions on Agent Trainer.
- **Autonomy Boundaries:** Simulation Agent: Fully autonomous within defined scenario context. Cannot access real customer data. Cannot initiate external communications.
- **Escalation Triggers:** AI change persona.
- **Audit Cadence:** Manager has adashboard too see anycorner case withing their agents a see the scoring and what went wrong, open a bug if there is something to be check by product team.
- **Shadow AI Audit (user-side):** 2 workarounds found · 1 build candidate build candidates · adjacent spend 100$ in chatGPT license to create scenarios.
- **Agent Boundaries:** | Agent | Can Do | Cannot Do | Approval Required | |-------|--------|-----------|-------------------| |Customer Simulation Agent| Simulate any persona in defined scenario context, adapt tone/language, escalate or de-escalate| Access real cu…
- **Regulatory Exposure:** EU AI Act: Limited risk category — training tool, human always in final evaluation loop

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):** Automate failure pattern detection — surface Scenario Gap Alerts to BA/CSM when >40% of agents fail a scenario type within 30 days
- **Horizon 2 (Next):** Native scenario generation from transcript — build scenario creation inside the platform, eliminating the ChatGPT workaround and reducing data exposure risk
- **Horizon 3 (Bet):** Vertical scenario libraries — pre-built, BA-validated scenario packs by industry (insurance, banking, telecom, healthcare) — accelerates onboarding, reduces BA cost per customer, creates a compounding product asset
- **Board Narrative:** Agent Trainer is the only AI simulation platform purpose-built for contact centers, combining multilingual voice emulation with proprietary skill evaluation to cut agent ramp time before they ever take a real call.
- **Ask:** Fund Horizon 2 and 3 — native scenario generation, LMS/CRM integrations, and in-platform analytics and Vertical scenario libraries.…
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

- **Compounding System:** [describe feedback loops]
- **Governance Posture:** [approach]
- **Shadow AI Status:** __ tools found, __ triaged
- **Agent Boundaries:**
- **Regulatory Exposure:**

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
- **Horizon 2 (Next):**
- **Horizon 3 (Bet):**
- **Board Narrative:** [1-sentence thesis]
- **Key Metric:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
