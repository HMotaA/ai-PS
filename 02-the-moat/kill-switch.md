# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Double dependency — Anthropic (Claude) for both simulation and evaluation engines and eleven labs for voices and languages| H  | develop own voice simulation |
| **Abstraction** | Direct API calls to both vendors, no abstraction layer| H  |Wrap both behind internal interfaces independently |
| **Routing** | | H / M / L | |
| **Eval** |Claude-dependent |M| Decouple eval prompts to be model-agnostic|

## Portability Score
Partial
<!-- Ready / Partial / Locked -->

## If ElevenLabs doubles pricing tomorrow:
They can´t. We have yearly pricelock
<!-- What's your 48-hour response? -->

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
Vertical expertise — they're a voice company, not a contact center company. They don't understand agent workflows, escalation patterns, or how to design a training scenario from a transcript
