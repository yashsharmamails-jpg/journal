# XAUUSD 15m → 1m Playbook (consolidated)

Synthesized from Gemini Prompt 3 + ChatGPT Prompt 3 outputs, plus baseline research.

> **Workflow:** Identify 15m liquidity → wait for 15m sweep → drop to 1m →
> enter on iFVG retest + BOS confirmation → target opposing 15m liquidity.

---

## 1. Session-by-session behavior (XAUUSD)

All times in UTC and IST. Times shift by 1 hour during DST (March–November).
Below uses **summer / DST** (current as of May 27, 2026).

| Session | UTC (DST) | IST | Avg ATR contribution | Behavior | Common trap |
|---|---|---|---|---|---|
| Sydney/Tokyo (Asia) | 22:00–06:00 prev | 03:30–11:30 | ~15–25% | Range-bound, algorithmic accumulation. Shallow sweeps (10–15 pts). Mean-reverting. | Believing an early Asian breakout is a real trend. 1m BOS continuation usually fails here. |
| Frankfurt / Pre-London | 06:00–07:00 | 11:30–12:30 | ~10–15% | "Judas swing" window. Asia high/low gets attacked. | Entering early on the Frankfurt push — it's often the fake. |
| London Open killzone | 07:00–10:00 | 12:30–15:30 | ~25–35% | True directional volume. Often creates the High or Low of the Day. | Fading the open without confirmation. |
| London-NY Overlap | 12:00–16:00 | 17:30–21:30 | ~40% (peak) | Maximum liquidity. Continuation + violent reversals. | Trading the news minute (CPI/NFP) — spread/slippage destroys 1m setups. |
| NY AM killzone | 12:00–15:00 | 17:30–20:30 | ~35–50% | COMEX open. Deep, violent sweeps (30–50 pts). USD data drives gold inversely. | Trading data release exact minute. |
| London Close | 15:00–17:00 | 20:30–22:30 | ~10–20% | Profit-taking, retracement against NY trend. | Late-session over-extension. |
| NY PM | 18:00–21:00 | 23:30–02:30 next day | ~5–10% | Tapering, consolidation. | Forcing trades in dead volume. |

---

## 2. Your specific window: Late Asia / Pre-London (10:00–14:00 IST)

This is the trader's home window. Honest assessment: **moderate-to-low edge, only tradeable with strict filters.**

### Tradeable conditions
1. **Asian range is ≥40 points top to bottom.** Tighter ranges = coiled spring → Frankfurt breaks it and trends without reversing.
2. **Price attacks the Asian high (BSL) or Asian low (SSL).** No middle-of-range trades — those are noise.
3. **Previous NY session did NOT end with a massive uncorrected momentum spike.** If it did, Asia drifts in that direction without producing actionable sweeps.
4. **15m sweep occurred** (mandatory precondition).

### Skip the window when
- Range < 40 points
- Yesterday closed with strong NY momentum that hasn't corrected
- No clear BSL or SSL has been touched
- Approaching news embargo windows (e.g. UK CPI at 06:00 UTC)

### Why this matters for you
Your first trade (`20260527-XAUUSD-01`) was in this window. The setup type was correct (lq grab + iFVG), but you didn't document whether the Asian range was ≥40 pts or which pool was attacked. Add these as mandatory checks going forward.

---

## 3. The 15m → 1m execution model (rigid rules)

### 3.1 Setting 15m bias
- **Look left:** Identify nearest unmitigated swing highs and lows on 15m. These are your BSL/SSL pools.
- **Premium/discount:** Where is current price relative to the dealing range?
- **Trigger:** Bias activates the **moment** a 15m candle wicks through a major liquidity pool. Don't wait for the close.

### 3.2 When 1m signals override 15m, and when they don't

| Condition | 1m action |
|---|---|
| Price consolidating in the middle of a 15m range | **Defer.** Ignore 1m iFVG/BOS — it's algorithmic noise. |
| 15m liquidity just got swept | **Trust the 1m.** A violent 1m BOS with displacement and iFVG overrides any prior 15m bias direction. |
| 15m is in a strong trend, no recent sweep | **Defer.** Don't fade 1m countertrend signals. |
| News pending in next 30 min | **Stand down.** Spread/slippage will invalidate 1m RR. |

### 3.3 iFVG on 1m XAUUSD — operational rules
- **Lifespan:** 5–15 minutes from formation. If price meanders 30+ min before retesting → algorithmic flow has shifted, skip.
- **Invalidation:** Body close completely outside the distal line of the iFVG. (Wicks are acceptable.)
- **Quality filter:** The BOS that created the iFVG must show displacement (1–2 large institutional candles, not a sluggish multi-candle grind).
- **Minimum mandate:** 1:2.5 RR. Anything less = stop too wide or entered too late in displacement.

### 3.4 Real BOS vs noise on 1m
- **Real BOS:** body close beyond the swing point that created the actual sweep low/high; large body, momentum.
- **Noise BOS:** wick-only break that closes back inside; break of inside-bar high/low; sluggish multi-candle grind.

### 3.5 Stop placement (XAUUSD-specific)
- **Spread:** 1.5–2.5 pips (15–25 points) typical, wider during news.
- **Slippage:** 5–10 points typical on entry/exit.
- **Buffer requirement:** Place stop **15–20 points beyond the sweep wick extreme**, not at the wick itself.
- **Why:** Algorithms routinely double-bottom 1m wicks to the decimal to wipe tight stops before reversing.

> **Example:** If 1m sweep low is exactly 4501.66, do NOT place stop at 4501.62.
> Place it at 4501.50 (≈16 pts buffer).

---

## 4. Psychological pitfalls + fixes

| Pitfall | Why it happens | Fix |
|---|---|---|
| Over-identifying iFVGs in ranging markets | 1m chart prints 60 candles/hour, gaps form constantly | **No 15m sweep = no 1m trade.** Tape this on monitor. |
| Forcing setups in low-volume Asia | Boredom in waking hours (10:00–14:00 IST) | Wait for Frankfurt 11:30 IST onwards. Let Tokyo build, let Frankfurt sweep. |
| Moving SL to BE too early | Eagerness to "lock in profit" | Only move to BE after **secondary 15m structure breaks** in your favor. Or take 50% partials at 1:2 and leave full stop. |
| Greed extension past HTF supply | "It looks like it'll run further" | Hard TP at opposing 15m BSL/SSL. Always. Take the money. |

---

## 5. Trade scoring rubric (10-point — Gemini-derived)

Every trade gets scored post-mortem. **Minimum passing score: 7/10.**

| # | Category | Points | What earns full marks |
|---|---|---|---|
| 1 | HTF Alignment | 2.0 | Trade triggered only after a clear 15m BSL or SSL sweep |
| 2 | Time Window | 1.0 | Inside London Open, NY AM, or Late-Asia *attacking range extreme* |
| 3 | Trigger Quality | 2.0 | 1m BOS with strong displacement; iFVG cleanly rejected on one side, respected on other |
| 4 | Stop Placement | 1.5 | 15–20 pt buffer beyond sweep wick |
| 5 | Target Placement | 1.5 | TP at unmitigated 15m FVG/OB or opposing liquidity pool — not arbitrary R |
| 6 | Trade Management | 1.0 | Followed predefined BE/partial rules; no fear-close |
| 7 | Journaling | 1.0 | Before SS (15m + 1m), after SS, emotion log |

> **Rule:** A losing trade scoring 8.5/10 is a **good trade** (statistical variance).
> A winning trade scoring 4/10 is a **terrible trade** (lucky) — behavior must be corrected immediately.

---

## Workflow diagram

```
                ┌─────────────────────────────────────┐
                │  D1/H4 bias set BEFORE session open │
                └────────────────┬────────────────────┘
                                 │
                ┌────────────────▼────────────────────┐
                │  Mark 15m BSL/SSL pools             │
                │  (unmitigated swings, equal H/L)    │
                └────────────────┬────────────────────┘
                                 │
                ┌────────────────▼────────────────────┐
                │  Wait for 15m wick through a pool   │
                │  (the "sweep")                      │
                └────────────────┬────────────────────┘
                                 │
                ┌────────────────▼────────────────────┐
                │  Drop to 1m                         │
                │  Wait for: BOS + displacement +     │
                │  iFVG creation                      │
                └────────────────┬────────────────────┘
                                 │
                ┌────────────────▼────────────────────┐
                │  Enter on retest of 1m iFVG         │
                │  Stop: 15–20 pts beyond sweep wick  │
                │  TP: opposing 15m pool, ≥1:2.5 RR   │
                └────────────────┬────────────────────┘
                                 │
                ┌────────────────▼────────────────────┐
                │  Manage: BE only after secondary    │
                │  15m structure breaks in your favor │
                │  OR take 50% at 1:2, full SL stays  │
                └────────────────┬────────────────────┘
                                 │
                ┌────────────────▼────────────────────┐
                │  Score post-trade (rubric)          │
                │  Log lessons in coaching/lessons.md │
                └─────────────────────────────────────┘
```

---

## Sources

- Gemini Prompt 3 deep research (XAUUSD playbook output, May 2026)
- ChatGPT Prompt 3 deep research (with citations to FXNX, TradingRage, Investopedia, May 2026)
- Cross-validated with baseline web research (TradingView session scripts, ICT mentorship summaries)

_Content was rephrased and consolidated for compliance with licensing restrictions._
