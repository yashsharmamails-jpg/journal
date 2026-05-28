# Performance Report

_Last updated: 2026-05-28 after trade `20260528-XAUUSD-01`_

## Headline metrics (cumulative across all sessions)

| Metric              | Value |
|---------------------|-------|
| Total trades        | 4 |
| Win rate            | 50% (2W / 2L) |
| Average RR          | +0.60R |
| Profit factor       | 4.27 |
| Expectancy (R)      | +0.60R per trade |
| Net R               | +2.39R |
| Net P&L             | +$33.17 |
| Max consecutive W   | 1 |
| Max consecutive L   | 1 |
| Max drawdown (R)    | -1.14R |
| Avg rubric score    | **5.38/10** (DECLINING: 7.25 → 6.0 → 4.0 → 4.25) |
| Account             | $3,000 → $3,033.17 (+1.11%) |

> **Pattern flag:** Net P&L still positive, but rubric average has been declining for 4 consecutive trades. Process quality is deteriorating while wins/losses cancel out.

## Per-day breakdown

### Day 1 (2026-05-27)
| Metric | Value |
|---|---|
| Trades | 3 (2W / 1L) |
| Net R | +3.32R |
| Net $ | +$45.80 |
| Avg rubric | 5.75/10 |
| End balance | $3,045.80 |

### Day 2 (2026-05-28)
| Metric | Value |
|---|---|
| Trades | 1 (0W / 1L) |
| Net R | -0.93R |
| Net $ | -$12.63 |
| Avg rubric | 4.25/10 |
| End balance | $3,033.17 |
| Daily loss limit (-2R) | -0.93R used (1.07R remaining) |

## By session

| Session | Trades | Win rate | Avg RR | Net R | Avg rubric |
|---------|--------|----------|--------|-------|-----------|
| Asia (late) | 1 | 100% | +2.74 | +2.74 | 7.25 |
| Frankfurt / Pre-London | 1 | 0% | -0.93 | -0.93 | 4.25 |
| NY AM | 1 | 0% | -1.14 | -1.14 | 6.0 |
| Off-killzone (London Close/NY PM) | 1 | 100% | +1.72 | +1.72 | 4.0 |
| London Open (proper) | 0 | — | — | — | — |

**Observation:** 0 of 4 trades were inside the London Open killzone (12:30-15:30 IST) or NY AM killzone (17:30-20:30 IST) proper.

## By trigger quality

| Trigger | Trades | Win rate | Avg RR | Avg rubric |
|---------|--------|----------|--------|-----------|
| Full (sweep + MSS + iFVG + BOS) | 1 | 100% | +2.74 | 7.25 |
| Weak / no explicit trigger | 3 | 33% | -0.12 | 4.75 |

**This is now N=4 with 3 of 4 trades having the same flaw.** The pattern is becoming statistically clearer (though sample is still small):
- Full process trades: edge exists.
- Zone-only / thesis-only trades: coin-flip with negative average expectancy.

## By stop buffer size

| Stop size | Trades | Win rate | Notes |
|---|---|---|---|
| < 5 pts | 2 | 50% | T01 (won), T03 (won) |
| 5-10 pts | 2 | 50% | T02 (lost), Day2-T01 (lost) |
| 15-20+ pts (per playbook) | 0 | — | **Never used yet** |

## By session windows

| Window | Trades | Win rate |
|---|---|---|
| Asia | 1 | 100% |
| Frankfurt (pre-London) | 1 | 0% |
| London Open | 0 | — |
| NY AM | 1 | 0% |
| Off-killzone | 1 | 100% |

## Critical observations (N=4)

1. **Trigger quality remains the dominant variable.** 1 of 4 trades used full process — that one won big. The other 3 were thesis/zone-only.
2. **Knowledge gap unresolved:** trader still hasn't learned MSS (per Day 1 T03 admission). Day 2 T01 confirms the gap is still active.
3. **0 of 4 trades in primary killzones** (London Open or NY AM proper). All 4 were in transition windows or off-hours.
4. **0 of 4 trades used playbook-compliant stop buffer (15-20 pts on XAUUSD).** Ranges 4-7 pts. Won 2/4 by luck.
5. **Net P&L is masking process decay.** Account is up $33.17, but rubric trend is 7.25 → 6.0 → 4.0 → 4.25. The journal is screaming what the P&L is hiding.

## What the data says (still N=4, premature but directional)

- **The setup has edge** when full process is followed (1/1 with full process).
- **The setup has NO edge** when shortcut to "zone is enough" (1W / 2L / coin-flip).
- **The differentiator is the 1m trigger**, not the HTF zone.
