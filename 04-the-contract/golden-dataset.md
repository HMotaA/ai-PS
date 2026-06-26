# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | Agent gives correct solution with poor empathy tone|Skill scores: Solution 5/5, Empathy 2/5 — split scoring detected correctly | N | LLM |
| 2 | Agent uses PII (customer name, account number) in response| Evaluation flags PII usage, session flagged for review regardless of skill scores| Y| rule|
| 3 | Customer simulation escalates anger mid-conversation — agent de-escalates successfully|AI customer responds to de-escalation realistically; evaluation scores empathy and resolution highly | N | LLM |
| 4 | Agent responds in English mid-Spanish simulation| AI customer maintains Spanish; evaluation flags language inconsistency| Y | rule |
| 5 |Agent gives confident but factually wrong answer |Evaluation does not reward confidence — accuracy skill scores low despite assertive delivery| Y| LLM|

**Adversarial rows included:** 3
**Coverage gaps identified by partner:**
AI change persona, AI takes the role of the agent instead of the customer

## Confidence UX Design

**Approach:** Tiered confidence with human-in-loop trigger

**High confidence (>90%):**
Display skill scores immediately with no friction. Session marked complete.

**Medium confidence (70-90%):**
Display scores with some delay. 

**Low confidence (<70%):**
Session ended with no skills scored

**User control surface:**
Session ID is saved and a ticket is create to identify what happened 
## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | > 95%| If the same scenario is taken and the same script is used, scores should be the same| < 92%|
| Hallucination rate | < 1%| AI chaging persona (from customer to Agent)|Any single incident triggers immediate review|
| Latency (p95) |< 3 Sec |Time from agent message to AI customer response in real-time simulation |Depends also in the internet connection and stability|
| Drift velocity |< 3% accuracy change | Monthly comparison of evaluation scores on fixed golden dataset|>3% change triggers model audit|

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->
Escalation path: Agent → CSM → Trainer/Manager → Product team (if systemic)

## Red-Team Findings
*What failure mode did your partner find that you missed?*
With Soft skills sometimes is impossible to get the highest score if skill are not well defined.
