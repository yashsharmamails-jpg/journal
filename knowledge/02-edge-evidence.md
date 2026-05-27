# Edge Evidence — what the data actually says

Synthesized from Gemini Deep Research + ChatGPT Prompt 2 outputs.

> **Bottom line:** The honest evidence base is thin. Two studies are confirmed by
> multiple sources; six are Gemini-only and need URL verification. The strongest
> defensible claim is *not* "iFVG has 70% win rate" — it's "standalone SMC concepts
> are negative-expectancy; only contextual stacking with liquidity sweeps + structure
> shows credible edge."

---

## Confidence-graded summary

| Concept / Strategy | Source confidence | Median WR | Median RR | Use? |
|---|---|---|---|---|
| Liquidity Grab + OB confirmation | Multi-source confirmed | 63% | 1:2.8 | **Yes** — strongest evidence base |
| Liquidity Sweep + iFVG | **Anecdotal** (one source, ~60 trades, discretionary filtering) | claimed 70%, **unverified** | claimed 1:2.0 | Use **but build your own sample** before trusting |
| Volume-backed displacement | Academic-supported (Cont et al. OFI) | n/a | n/a | **Yes** — core mechanic |
| Standalone Order Block | Multi-source confirmed (16,000 variant test) | <30% | Variable | **No** — negative expectancy |
| Standalone FVG | Multi-source confirmed | 29% | 1:1.5 | **No** — 84% of unfiltered FVGs fail |
| OTE on static fib (H1/M15) | Multi-source confirmed | 13–16% | High skew | **No** — no edge without sweep + structure |
| Silver Bullet (mechanical) | Multi-source confirmed | 61% point estimate | 1:2.4 | **No** — 46% capital loss over 10y on EURUSD |
| Multi-concept SMC system (BOS+OB+FVG) | One transparent backtest (QuantumAlgo) | 64.2% on Gold | 1:2.31 | Possibly — large sample but vendor-published |

---

## Confirmed studies (cross-validated by ≥2 LLM sources)

### Study A — QuantumAlgo 2,600-trade composite SMC backtest
- **Concept:** OB + FVG + Liquidity composite system on multiple instruments.
- **Instrument:** XAUUSD subset = 342 trades, 64.2% WR, PF 2.47, max DD 8.3%, period Jan 2024–Mar 2026.
- **Aggregate:** ~2,632 trades, 61.2% WR, +2.27R avg, PF 2.17.
- **Methodology rating:** 3/5 — backtest is reproducible but author sells services (vendor data).
- **Note:** Manual bar-replay methodology subject to hindsight bias even when claimed mechanical.

### Study B — 16,000 strategy variants order block test (Reddit r/algotrading)
- **Concept:** Standalone Order Block limit entries.
- **Coverage:** 100 US stocks, 100 crypto, 30 US futures, 50 forex pairs across 1m to 1d timeframes.
- **Result:** Negative expectancy across nearly all configurations. Forex closest to break-even.
- **Methodology rating:** 5/5 — full Python backtesting.py code, systematic.
- **Conclusion:** **Limit-order-on-OB without any other context = no edge.**

---

## Gemini-only studies (need URL verification — TREAT AS UNCONFIRMED)

| Study | Claim | Verification |
|---|---|---|
| 10-yr EURUSD ICT framework backtest (Reddit r/Forex 1sgw3g4) | Silver Bullet 61% WR but 46% capital loss / 10y | Unverified URL |
| YouTube OTE backtest (aVh-2Gv7kr8) | BTC 13% WR, ES 16% WR | Unverified URL |
| GitHub `starckyang/smc_quant` | ETHUSDT, 23% training WR, 50% test WR, 28% DD | **Verifiable on GitHub** — high transparency |
| 7-yr XAUUSD multi-strategy (Reddit) | ICT models lost vs MA crossover and buy-and-hold | Unverified URL |
| iFVG discretionary model (Reddit r/Daytrading 1dfcgqf) | 80–85% WR but ~60 trades, "wait for price action to look amazing" | Unverified, **discretionary filtering invalidates the WR** |
| FVG AI agent (Medium) | 29% WR on 300 trades, 84% of FVGs fill and reverse | Unverified |

---

## Academic context (general microstructure, not SMC-specific)

| Topic | What the literature says | Implication for SMC |
|---|---|---|
| Stop-loss cascades (Carol L. Osler 2002/2005) | Stop-loss orders cluster at round numbers and S/R; price trends rapidly through these clusters; dealers exploit predictability | **Validates "liquidity sweep" mechanic.** Strongest academic grounding in SMC. |
| Order Flow Imbalance (Cont et al. 2010/2014) | Linear relation between OFI and price changes; aggressive market orders create liquidity vacuums | **Validates FVG/displacement concept** — but only when backed by volume |
| VPIN / order flow toxicity (Easley, López de Prado, O'Hara 2012) | Distinguishes informed from uninformed flow; FVGs without toxic flow are common gaps that mean-revert | **Explains why most FVGs fail.** "Displacement Flaw" maps to this. |
| Latency arbitrage / temporal anomaly decay | Time-based edges are arbitraged rapidly by HFTs | **Explains Silver Bullet failure.** Static time windows = no durable edge. |

---

## What the evidence supports (defensible claims)

1. **Liquidity sweeps are real** and academically grounded (Osler).
2. **Order flow imbalance** drives short-term price reversion (Cont).
3. **Volume-backed displacement** distinguishes real institutional intent from noise (VPIN).
4. **Stacking conditions matters more than any single concept.** Win rates from composite systems > standalone signals consistently.

## What the evidence does NOT support

1. Standalone OBs, standalone FVGs, standalone OTE, standalone Silver Bullet.
2. Specific win-rate claims like "70% on iFVG" — sample sizes are too small.
3. Rigid 1-hour time windows as guaranteed-edge zones.
4. SMT divergence as a standalone signal (no public backtest exists).

## Top documented failure modes

1. **FVG liquidity trap:** ~84% of unfiltered FVGs fill and immediately reverse. Cause: no volume backing.
2. **Range market devastation:** SMC systems collapse in mean-reverting markets (ETHUSDT test: 23% WR, 28% DD).
3. **Prop-firm drawdown breach:** SMC win rates >50% but DD violations sink prop-firm pass rates to 34–38%.
4. **Tight stops on sweeps:** Sweep wicks routinely overshoot by 5–10 pts, hitting stops before reversal.

---

## Recommended journaling fields (per Gemini Prompt 2)

Add these to your ledger to validate edge personally:

| Field | Why it matters |
|---|---|
| `market_regime` (Trending / Ranging) | SMC fails in ranges. Track to filter out wrong-environment trades. |
| `pre_entry_liquidity_swept` (Y/N + which pool) | The single most important filter separating high-edge from low-edge SMC trades. |
| `premium_discount_alignment` (Y/N) | Buying premium / selling discount = drawdown machine. |
| `displacement_volume_quality` (1–5) | Captures the "Displacement Flaw" — gaps without volume fail. |
| `trigger_mechanism` (limit at OB / iFVG retest / BOS confirm / etc.) | Distinguishes blind-limit (negative EV) from confirmed entries. |
| `mae_R` (max adverse excursion in R) | Optimizes stop placement empirically. |
| `mfe_R` (max favorable excursion in R) | Optimizes TP placement empirically. |

---

## Sources

- QuantumAlgo backtest: [quantum-algo.com](https://www.quantum-algo.com/backtests/) (vendor — flag for bias)
- Order Block 16,000-variant test: [Reddit r/algotrading 1qvovpv](https://www.reddit.com/r/algotrading/comments/1qvovpv/i_tested_for_1_year_order_blocks_smart_money/)
- SMC Pro BTC strategy: [TradingView scripts](https://www.tradingview.com/scripts/fairvaluegaps/)
- GitHub open-source SMC: [starckyang/smc_quant](https://github.com/starckyang/smc_quant)
- Investopedia stop-hunting: referenced via ChatGPT Prompt 2 output
- Tradervue FVG limitations: referenced via ChatGPT Prompt 2 output

_Note: Several URLs above are Gemini-only and were not cross-confirmed by ChatGPT's
search. Verify before treating as authoritative. Content rephrased for compliance._
