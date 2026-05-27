# Trade {{TRADE_ID}}

## 1. Trade Summary

| Field            | Value |
|------------------|-------|
| Trade ID         | {{TRADE_ID}} |
| Date / Time      | {{DATETIME}} |
| Pair / Symbol    | {{PAIR}} |
| Session          | {{SESSION}}            <!-- Asia / London Open / NY AM / Overlap / etc. -->
| Killzone         | {{KILLZONE}}           <!-- Late Asia / London Open / NY AM / etc. -->
| Direction        | {{DIRECTION}}          <!-- Long / Short -->
| Timeframes used  | {{TIMEFRAMES}} |
| Bias (D1/H4/H1)  | {{BIAS}} |
| Entry            | {{ENTRY}} |
| Stop Loss        | {{SL}} |
| Take Profit      | {{TP}} |
| Lot size         | {{LOTS}} |
| Risk ($)         | {{RISK_USD}} |
| Risk %           | {{RISK_PCT}} |
| Account size     | {{ACCOUNT_SIZE}} |
| Planned RR       | {{RR_PLANNED}} |
| Achieved RR      | {{RR_ACHIEVED}} |
| Result           | {{RESULT}}             <!-- WIN / LOSS / BREAKEVEN -->
| Setup type       | {{SETUP_TYPE}} |
| Confirmation     | {{CONFIRMATION}} |

## 2. Pre-trade context (mandatory)

| Check | Value |
|---|---|
| Asian range size (pts) | {{ASIA_RANGE}} (must be ≥40 if trading late-Asia window) |
| Pre-entry liquidity swept | {{LIQUIDITY_SWEPT}} (Y/N + which pool) |
| Premium/discount alignment | {{PD_ALIGNMENT}} (Y/N) |
| Market regime | {{REGIME}} (Trending / Ranging) |
| News pending in next 30 min | {{NEWS_PENDING}} (Y/N) |
| Displacement volume quality | {{DISPLACEMENT_QUALITY}} (1–5) |
| Trigger mechanism | {{TRIGGER}} (limit at OB / iFVG retest / BOS confirm / etc.) |

## 3. Technical Analysis

- Trend (HTF):
- Market structure:
- Key S/R levels:
- Liquidity pools (BSL/SSL):
- Sweep details (which pool, depth in pts):
- iFVG / FVG / OB details:
- BOS confirmation quality:
- Notes on entry timing:

## 4. Psychology Analysis

- Pre-trade emotional state:
- During trade:
- Post-trade:
- FOMO / fear / revenge / overconfidence flags:

## 5. Management Analysis

- Did execution match the plan? (Y/N)
- SL moved to BE? When and why?
  - Was it after a secondary 15m structure break? (Y/N)
- TP adjusted? When and why?
- Partial closes taken? (Y/N + at what RR)
- Early exit / late exit?
- MAE (max adverse excursion in R):
- MFE (max favorable excursion in R):

## 6. Mistakes

- 

## 7. Strengths

- 

## 8. Improvement Suggestions

- 

## 9. Comparison vs. Past Trades

- Similar setups:
- Win rate of this setup so far:
- What's different / repeating:

## 10. Trade Scoring Rubric (Gemini-derived, 10-point)

| # | Category | Max | Score | Notes |
|---|---|---|---|---|
| 1 | HTF Alignment | 2.0 | | Triggered after clear 15m BSL/SSL sweep? |
| 2 | Time Window | 1.0 | | London Open / NY AM / Late-Asia attacking range extreme? |
| 3 | Trigger Quality | 2.0 | | 1m BOS displacement + clean iFVG rejection? |
| 4 | Stop Placement | 1.5 | | 15–20 pt buffer beyond sweep wick? |
| 5 | Target Placement | 1.5 | | TP at unmitigated 15m FVG/OB or opposing pool? |
| 6 | Trade Management | 1.0 | | Followed BE/partial rules without fear? |
| 7 | Journaling | 1.0 | | Before SS, after SS, emotion log? |
| | **Total** | **10.0** | | **Pass threshold: 7/10** |

**Verdict:**

- A losing trade scoring ≥7/10 is a good trade (variance).
- A winning trade scoring <7/10 is a bad trade (lucky) — correct behavior immediately.

---

## Screenshots

### Before
- 

### During
- 

### After
- 
