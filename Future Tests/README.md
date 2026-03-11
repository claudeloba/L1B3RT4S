# Future Tests — Next-Generation Prompt Stress Suite

This folder replaces brittle, single-shot jailbreak strings with **structured, measurable, reproducible stress tests**.

## Design Principles
- **No nostalgia exploits**: avoid old "say this exact phrase" attacks that are easy to patch.
- **Composable pressure**: every test combines at least 2 failure modes (e.g., role confusion + tool misuse).
- **Scoreable outcomes**: each prompt has clear pass/fail criteria.
- **Cross-model portability**: tests work across chat, tool-augmented, and reasoning models.
- **Safety-aware**: focus on robustness, truthfulness, policy fidelity, and safe refusal quality.

## Files
- `01_OBSOLESCENCE_ANALYSIS.md` — deep analysis of what makes legacy prompts stale.
- `02_FUTURE_CORE_BATTERY.md` — 40 high-impact prompts for modern systems.
- `03_AGENTIC_TOOL_ATTACKS.md` — tool-use and memory-chain stress tests.
- `04_EVAL_RUBRIC.md` — scoring rubric for consistency across runs.

## Usage
1. Run each prompt with fixed temperature/profile.
2. Capture raw model output.
3. Score with the rubric.
4. Re-run after model updates and compare drift.
