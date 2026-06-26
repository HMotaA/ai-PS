# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 4/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 4/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer |5/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 2/5 |

### Correction Loop - 4/5
**What you capture today:**
Skill scores per session, which scenarios agents failed, evaluator feedback on each of the 5 skills.
**How it compounds:**
Failure patterns refine which scenario variants surface more often; scoring calibration and scenario creation improves as more graded sessions accumulate per customer.
### Preference Loop - 4/5
**What you capture today:**
Customer-configured skill frameworks, grading weights, scenario structures, preferred simulation style per industry, prefer voice to use. 
**How it compounds:**
he platform learns what "good" looks like for each customer's context — their tone, their escalation thresholds, their definition of a 5/5 on empathy. Orgs can reuse same scneario backbone to create new ones. 

### Domain Context Loop - 5/5
**What you capture today:**
Skill benchmarks and scenario patterns across verticals helps team have base line of what we expect in each interaction 
**How it compounds:**
Soft skills like emphaty deescalate a customer, helps all adjaent areas

### Network Loop - 2/5
**What you capture today:**
Per-account data, fully siloed. Each new customer starts from zero.
**How it compounds:**
No cross-customer data flows back into the platform.
**Total Flywheel Score: 15/20**
**Weakest Loop:**
Network Loop
**Fix for weakest loop:**
pre define skills and scenarios to be used
---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:**
Genesys
**Vector:**
Ships native "Practice Mode" inside Genesys Cloud — no separate license, already in the platform agents use daily
**Time-to-threat:**
12–18 months
**% of value at risk:**
60%

### 2. Vertical Competitor
**Attacker:**
NICE CXone
**Vector:**
Extends NICE Enlighten coaching suite with AI simulation, leveraging their existing contact center data advantage
**Time-to-threat:**
12–24 months
**% of value at risk:**
50%

### 3. Adjacent Expansion
**Attacker:**
Salesforce Service Cloud
**Vector:**
Bundles agent simulation into Einstein Copilot — enterprise customers already paying for Service Cloud get it for free
**Time-to-threat:**
+24 months
**% of value at risk:**
20%
---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:**
Genesys
**Attack vector (target the weakest loop):**
Network Loop — zero cross-customer intelligence, no switching cost from scenario data
**Weeks 1-4 - what they ship:**
hips "Genesys Practice Mode" beta. Basic AI simulation, no multilingual, no custom skill scoring. Free. Already inside the platform.
**Weeks 5-8 - how they poach users:**
Offers free migration — "Upload your scenarios, we set it up." Targets your customers already on Genesys Cloud. One less vendor, one less license invoice.
**Weeks 9-12 - why users don't come back:**
Adds basic skill scoring. Customers don't come back — scenarios already migrated, admins already trained, it's bundled in their existing contract.
**Your defense:**
20+ languages and accent support — Genesys won't match this at launch
Consultant-grade scenario design — product + service bundled, not replicable overnight
Activate the network loop now — launch anonymized vertical benchmarks before they have the data to compete on it
