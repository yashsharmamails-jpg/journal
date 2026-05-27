# ICT / SMC Concept Reference (consolidated)

This is the synthesized reference, built from 4 deep-research outputs (Perplexity,
ChatGPT structured, ChatGPT Deep Research with citations, Gemini quantitative).
Where sources disagree, the strictest defensible rule is used.

> **Use this file as the source of truth when grading any future trade.**

---

## Quick lookup

| # | Concept | One-line meaning | Use case for you (15m/1m XAUUSD) |
|---|---|---|---|
| 1 | BOS | Continuation: trend extends past prior swing | Confirm 1m entry direction matches 15m |
| 2 | CHoCH | First reversal warning | Early exit signal on a runner |
| 3 | MSS | Reversal-grade break with displacement | Your primary entry trigger |
| 4 | Liquidity pools | Stop clusters above highs / below lows | Map these on 15m before any entry |
| 5 | Liquidity sweep / Judas swing | Wick beyond pool, immediate rejection | The required setup precondition |
| 6 | Order Block (OB) | Last opposing candle before displacement that breaks structure & leaves FVG | Refined entry zone |
| 7 | Breaker block | Failed OB flipped to opposite role | Reversal continuation |
| 8 | Mitigation block | Same-direction OB retest, body holds | Trend-continuation refinement |
| 9 | FVG / Imbalance | 3-candle gap from displacement | Entry zone after MSS |
| 10 | iFVG | FVG closed through, polarity flipped | **Your specific edge** |
| 11 | BPR | Bull FVG + Bear FVG overlap | Tight reaction zone, rare |
| 12 | OTE / PD | 0.62–0.79 fib retracement; >50% = premium | Skip standalone (no edge) |
| 13 | Power of Three | Accumulate → manipulate → distribute | Day-framing model |
| 14 | Displacement | Strong impulsive move ≥1.5–2× ATR | Required for valid MSS |
| 15 | Killzones | High-liquidity time windows | Trade only inside these |
| 16 | Silver Bullet | 1-hr precision window | Skip mechanical use (negative edge) |
| 17 | Daily bias | D1 → H4 → H1 hierarchy | Set before market open |
| 18 | ICT 2022 model | Bias → sweep → MSS → FVG entry → 1:3 RR | Your workflow |
| 19 | ICT 2024 model | 2022 + tighter time/CISD focus | Refinement layer |
| 20 | SMT divergence | Correlated assets fail to confirm | Confluence only, not standalone |

---

## Killzones (master table — handles DST)

ICT killzones are anchored to **New York local time**. Convert to UTC and IST below.

| Killzone | NY local time | UTC (winter, EST=UTC−5) | UTC (summer, EDT=UTC−4) | IST (UTC+5:30) — winter | IST — summer |
|---|---|---|---|---|---|
| Asia | 19:00–24:00 | 00:00–05:00 | 23:00 prior day–04:00 | 05:30–10:30 | 04:30–09:30 |
| London Open | 02:00–05:00 | 07:00–10:00 | 06:00–09:00 | 12:30–15:30 | 11:30–14:30 |
| London Silver Bullet | 03:00–04:00 | 08:00–09:00 | 07:00–08:00 | 13:30–14:30 | 12:30–13:30 |
| NY AM | 07:00–10:00 | 12:00–15:00 | 11:00–14:00 | 17:30–20:30 | 16:30–19:30 |
| NY AM Silver Bullet | 10:00–11:00 | 15:00–16:00 | 14:00–15:00 | 20:30–21:30 | 19:30–20:30 |
| London Close | 10:00–12:00 | 15:00–17:00 | 14:00–16:00 | 20:30–22:30 | 19:30–21:30 |
| NY Lunch | 12:00–13:00 | 17:00–18:00 | 16:00–17:00 | 22:30–23:30 | 21:30–22:30 |
| NY PM | 13:00–16:00 | 18:00–21:00 | 17:00–20:00 | 23:30–02:30 next day | 22:30–01:30 next day |
| NY PM Silver Bullet | 14:00–15:00 | 19:00–20:00 | 18:00–19:00 | 00:30–01:30 next day | 23:30–00:30 next day |

**DST window in US:** 2nd Sunday of March → 1st Sunday of November.
On May 27, 2026 (DST active), London Open killzone is **06:00–09:00 UTC = 11:30–14:30 IST**.

---

## Per-concept rules (only the parts that matter for trading XAUUSD 15m/1m)

### 1. Break of Structure (BOS) — continuation
- Bullish: candle **body** closes above prior external swing high in an HH-HL sequence.
- Bearish: body close below prior swing low in LH-LL sequence.
- Wick-only breaks are invalid.
- Required strength: break candle body ≥ **1.5× ATR(20)** of prior 10 candles.
- Highest probability: London Open or NY AM, after liquidity sweep.

### 2. Change of Character (CHoCH) — early reversal warning
- Bearish CHoCH: in uptrend (HH-HL-HH), price body closes below the protected HL.
- Bullish CHoCH: in downtrend (LL-LH-LL), body closes above protected LH.
- Best validity: occurs immediately after a liquidity sweep at HTF premium/discount.
- Without the sweep, downgrade to "noise."

### 3. Market Structure Shift (MSS) — reversal-grade
**Strictest combined rule (all 3 sources agree):**
1. Liquidity sweep occurred first.
2. Body close beyond opposing structural swing.
3. Displacement: break candle ≥ 2× ATR(20) AND body ≥ 80% of candle range AND leaves an FVG.

If any of the 3 fails → not MSS, downgrade to CHoCH or noise.

### 4. Liquidity pools
- Buy-side (BSL): above swing highs, equal highs (≤0.05% AND ≤10% of 15m ATR apart), trendline highs (≥3 touches).
- Sell-side (SSL): mirror.
- Rank by visibility: daily/session extremes > equal highs/lows > trendline > internal pivots.

### 5. Liquidity sweep / Judas swing
- Wick or brief close beyond a marked pool, then rejection within 1–5 candles.
- High-quality sweep: excursion 0.10–0.40× 15m ATR. Larger = real breakout, not sweep.
- "Judas swing" specifically: first 90 min of London or NY, attacks one side then reverses.

### 6. Order Block (OB) — strict 3-criteria
1. Last opposing candle before impulse (last bearish before rally, or last bullish before drop).
2. Following move creates a valid FVG.
3. Move causes BOS or MSS within 1–5 candles.
- Void if price closes through opposite extreme of the candle before reaction.

### 7. Breaker block
- Old OB invalidated by body close beyond opposite extreme + opposing MSS = breaker.
- Retest from opposite side, no full close through far edge on first retest.

### 8. Mitigation block
- OB tested by retracement, body **does not** close beyond OB extreme. Trend resumes.
- If body closes through → it's a breaker, not mitigation.

### 9. Fair Value Gap (FVG)
- 3-candle pattern: bullish FVG = candle 3 low > candle 1 high.
- Minimum size: gap width ≥ 0.05× 15m ATR or 20% of displacement candle body.
- Lifespan: fresh ≤20 candles on 1m, ≤10 candles on 15m. Archive after 50% mitigated.

### 10. Inverse FVG (iFVG) — your edge
**Strict rule (most contested concept across sources, use the strictest):**
- Existing FVG must be **fully closed through** by a candle body in opposite direction.
- The closing move must include displacement (≥1.5× ATR).
- Retest from the new side must hold on a closing basis ≥1 candle.
- Must be accompanied by MSS or BOS in the new direction.
- If only filled (no body close beyond far edge) = consumed, not inverted. Skip.

### 11. Balanced Price Range (BPR)
- Overlap of opposing valid FVGs from same intraday context.
- Use only as refinement, not primary trigger. Rare on 1m.

### 12. Premium / Discount + OTE
- 50% of dealing range divides premium (above) and discount (below).
- OTE zone: 0.62–0.79 fib, sweet spot at 0.705.
- **Standalone OTE has no edge** (per Prompt 2 evidence). Use only as refinement inside an MSS/sweep setup.

### 13. Power of Three (PO3)
- Daily candle anatomy: accumulation (Asia) → manipulation (London open Judas) → distribution (NY).
- Anchor to **00:00 ET (true daily open)** per Gemini.
- Useful as day-framing, not as standalone signal.

### 14. Displacement (objective)
- True Range ≥ 2.0× ATR(20) on the operating timeframe.
- Body ≥ 80% of candle range.
- Close in top quartile (bullish) or bottom quartile (bearish).
- Required for valid MSS.

### 15. Killzones — see master table above

### 16. Silver Bullet — caution
- 1-hour precision windows nested inside killzones.
- **Mechanical Silver Bullet had a 46% capital loss over 10 years on EURUSD** in the algorithmic study (Prompt 2). Treat as low-edge unless paired with full MSS + FVG + bias alignment.

### 17. Daily bias derivation
- D1: external draw on liquidity (above or below). Set bias bullish/bearish/neutral.
- H4: confirm structural condition. Map premium/discount within current dealing range.
- H1: locate intraday liquidity pools (PDH/PDL, equal H/L).
- Execution rule: only take 1m setups aligned with the combined D1/H4/H1 narrative.

### 18. ICT 2022 model — your workflow
1. Daily bias from D1/H4.
2. Mark reference range (e.g. NY midnight to London open).
3. Wait for liquidity sweep against bias.
4. Confirm MSS with displacement on 1m–5m, leaving FVG.
5. Mark the PD array (FVG, OB, iFVG, breaker).
6. Verify PD array sits in correct premium/discount zone.
7. Enter on retrace into the PD array.
8. Stop beyond sweep extreme + buffer (see playbook).
9. Target opposing intraday liquidity pool.
10. Min RR 1:3 (or 1:2.5 for tight 1m setups per playbook).

### 19. ICT 2024 model — refinements
- Tighter time-of-day filter (08:30 ET preparation).
- Concept candidate: **CISD (Change in State of Delivery)** — currently unverified across sources, treat as experimental.
- Same execution spine as 2022 model.

### 20. SMT divergence
- For XAUUSD: cross-reference DXY (inverse) or XAGUSD (positive correlation).
- Bullish SMT: XAUUSD makes LL, paired asset fails to confirm.
- Use as confluence at HTF liquidity points only, never standalone.

---

## Cross-source disagreement log

| Topic | Resolution |
|---|---|
| BOS displacement threshold | 1.5× ATR(20), body close in top/bottom third |
| MSS displacement threshold | 2× ATR(20) AND body ≥80% range AND must leave FVG |
| FVG lifespan | Fresh ≤20 candles on 1m, ≤10 on 15m, archive at 50% mitigated |
| iFVG inversion vs consumption | Body close beyond far edge required (not wick), plus MSS/BOS |
| Asia killzone exact UTC | Use NY-local-time anchor (7 PM–midnight ET) and convert per DST |
| Equal H/L tolerance | 0.05% AND ≤10% of 15m ATR (whichever stricter) |
| ICT 2024 model | No formal new model; CISD is candidate concept, unverified |
| Silver Bullet | Mechanical use = negative edge over 10y; only valid with full MSS+FVG+bias |
| Standalone OB | No edge per 16,000-variant test; require sweep + structure |
| Standalone OTE | No edge per BTC/ES tests (13–16% WR); require sweep + structure |
| Liquidity Sweep + iFVG win rate | Claimed 70% but only one Reddit source ≤60 trades — **anecdotal until you build your own ≥30 sample** |

---

## Sources

- ICT 2022 mentorship summary: [tradeify.co](https://tradeify.co/post/ict-concepts-for-prop-firm-trading-and-passing-evaluations)
- iFVG technical: [fluxcharts](https://www.fluxcharts.com/articles/inversion-fair-value-gaps-ifvg-explained), [mql5 article](https://www.mql5.com/en/articles/16659)
- XAUUSD session behavior: [Liquidity Sweep TradingView script](https://tr.tradingview.com/scripts/liquidity/)
- Statistical critique: [lunetrading order block backtests](https://www.lunetrading.com/blog/best-order-block-indicators-2026-tradingview-top-picks-backtests-win-rates)
- Honest critique: [mindmathmoney ICT review](https://www.mindmathmoney.com/articles/ict-trading-concepts-explained-the-truth-without-the-hype)
- Stop-hunt academic context: Carol L. Osler 2002/2005 (cited via Gemini Prompt 2 output)
- Order Flow Imbalance: Cont et al. 2010/2014 (cited via Gemini Prompt 2 output)
- VPIN / order flow toxicity: Easley, López de Prado, O'Hara 2012 (cited via Gemini Prompt 2 output)

_Content was rephrased and consolidated from multiple LLM deep-research outputs for compliance with licensing restrictions. Where direct claims are made about academic literature, the user should verify the cited papers independently before relying on those numbers._
