# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference Claude (primary model) |$2–4 | ~20 sessions, Sonnet pricing for simulation and detailed evaluation|
| Inference (cascading/triage) | $8–15|Largest cost driver — scales directly with session volume |
| Infrastructure | $3–5| Cloud hosting, APIs, session management|
| Data/storage | $0.50–1| |
| Human-in-the-loop (Customer Success Manager, Project Manager, Business Analyst)| 15$| Scales inversely with account size — smaller accounts cost more per seat|
| **Total AI COGS** | $29 - 46| |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:**
Claude Haiku

**Frontier model:**
Claude Sonnet

**Routing rule:**
Basic yes/no skill checks and simple grading → Haiku. Full customer persona simulation, nuanced skill evaluation, and multi-turn conversations → Sonnet.

**Expected cascade ratio:**
30% Haiku / 70% Sonnet

## Pricing Model

**Current pricing:**
Per license (seat-based)

**Proposed AI pricing:**
Hybrid — base seat fee + usage tier above a session threshold

**Model:** seat-based / usage-based / outcome-based / hybrid
hybrid

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x |Claude: minor — adds ~$6–12/user. ElevenLabs: critical — voice jumps to $24–45/user, potentially margin-negative | Activate fallback voice provider immediately; enforce session caps on lower tiers|
| Heaviest segment doubles |Power users double session count — ElevenLabs cost doubles, CSM load increases, seat revenue stays flat | ntroduce session tier pricing; heavy-use periods trigger usage-based billing|
| Model provider raises prices 50% | Claude +50%: ~$1.50–3 impact/user — absorbable. ElevenLabs +50%: ~$4–7.50 impact/user — meaningful margin erosion on top of already high COGS|Negotiate more than 1 year contract with pricelock for leven labs|

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
Per-seat recurring revenue. Predictable COGS. No onboarding revenue. Gross margin 70–80%.
**After (AI-enabled):**
Two revenue streams — $15,000 onboarding fee (one-time, margin-positive, funds BA) + per-seat recurring. Gross margin 35–55% on recurring depending on account size and session volume. Onboarding margin offsets customer acquisition cost.
**Net margin shift:**
Onboarding helps us train their team, so they can maximice value, hence more license are purchase, most of the time they do a pilot, if they see the value they will adquire more license
