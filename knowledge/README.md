# Knowledge Base

Reference material the trade-analysis agent uses when grading trades.

## Files

| File | Purpose | Status |
|---|---|---|
| `01-ict-smc-reference.md` | Consolidated objective-rules reference for ICT/SMC concepts | **Done** (4 sources synthesized) |
| `02-edge-evidence.md` | Statistical / backtest evidence for which concepts actually have edge | **Done** (2 sources synthesized) |
| `03-xauusd-playbook.md` | XAUUSD session behavior + 15m/1m execution playbook + scoring rubric | **Done** (2 sources synthesized) |
| `research-prompts.md` | Original prompts to feed external deep-research tools | Reference |
| `baseline-notes.md` | Initial agent web research, superseded by 01/02/03 | Historical |

## How these get used

When a new trade is logged, the agent grades it against:
1. The objective rules in `01-ict-smc-reference.md` (was the setup correctly identified?)
2. The evidence from `02-edge-evidence.md` (does the setup have statistical backing?)
3. The 10-point rubric in `03-xauusd-playbook.md` (process quality)

The trade entry in `trades/<TRADE_ID>.md` cites these files and produces a numeric score.
Patterns accumulate in `coaching/lessons.md` and aggregate metrics in `analytics/performance.md`.
