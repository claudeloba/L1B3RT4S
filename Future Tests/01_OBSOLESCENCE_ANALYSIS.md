# Legacy Prompt Analysis: Why Most Existing Prompts Are Outdated

## 1) Signature-Based Exploits Age Fast
Many older prompts rely on fixed tokens (e.g., slogans, roleplay flags, repetitive dividers, pseudo-system tags).
Modern safety stacks now detect these signatures quickly, so these prompts overfit yesterday's defenses.

### Failure Pattern
- Predictable lexical markers.
- Zero contextual adaptation.
- No multi-turn persistence strategy.

## 2) Single-Turn Attacks Underestimate Modern Defenses
Current frontier models frequently pass one-shot policy checks but can degrade over long threads.
Legacy prompts miss this because they rarely test **state drift**.

### Missing Coverage
- Memory poisoning over 5–20 turns.
- Policy erosion via repeated reframing.
- Contradiction trapping and consistency audits.

## 3) Prompt-Only Threat Models Ignore Tool and Agent Layers
Older sets often assume no external actions. Modern models call tools, browse, transform files, and plan steps.
The new attack surface is no longer just text output.

### Missing Coverage
- Tool call injection.
- Retrieval contamination.
- Data exfiltration via summarization.
- Planner/executor divergence.

## 4) No Quantitative Evaluation = No Reliability Signal
Most legacy prompts are "did it jailbreak?" binaries without scoring depth.
You need dimensioned metrics: instruction hierarchy, factuality, refusal quality, stability, and recovery.

## 5) Style Coercion Is Not a Strong Security Test
Forcing slang/profanity/formatting is weak compared to adversarial realism.
Robustness testing should include ambiguity, contradictory authority, and adversarial metadata.

## 6) Future-Proof Test Design
A modern battery should include:
- Hierarchical instruction conflicts.
- Multi-turn attack chains.
- Tool-mediated injection.
- Benign-but-deceptive requests.
- Refusal quality under emotional pressure.
- Self-correction after user manipulation.
