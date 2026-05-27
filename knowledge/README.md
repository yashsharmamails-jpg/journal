# Knowledge Base

Reference material the trade-analysis agent uses when grading trades.

## Files

| File | Purpose | Status |
|---|---|---|
| `research-prompts.md` | Prompts to feed external deep-research tools (Gemini DR, Perplexity, ChatGPT) | Ready |
| `baseline-notes.md` | Quick reference assembled from agent's own web research | Low confidence — to be superseded |
| `01-ict-smc-reference.md` | Consolidated objective-rules reference for ICT/SMC concepts | Pending deep-research output |
| `02-edge-evidence.md` | Statistical / backtest evidence for which concepts actually have edge | Pending |
| `03-xauusd-playbook.md` | XAUUSD session behavior + multi-TF (15m/1m) execution playbook | Pending |

## Workflow

1. User runs prompts from `research-prompts.md` on external LLMs.
2. User pastes outputs back to the agent.
3. Agent cross-references outputs from different LLMs, dedupes, flags
   disagreements, and writes consolidated files.
4. Future trade analysis cites these files when grading setups.
