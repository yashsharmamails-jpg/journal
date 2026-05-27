# Baseline ICT/SMC Notes

Quick reference assembled from the agent's own web research, before the
deep-research outputs land. To be superseded by `01-ict-smc-reference.md`,
`02-edge-evidence.md`, `03-xauusd-playbook.md` once those are produced.

Sources are cited inline. Treat this file as low-confidence until verified.

## Canonical concepts (what the term means)

| Concept | One-line meaning |
|---|---|
| BOS | Price breaks the most recent swing high (bull) / low (bear) — confirms trend continuation |
| CHoCH | First counter-trend break of structure — early reversal signal |
| MSS | Stronger reversal signal: counter-trend break with displacement (impulsive candle) |
| Liquidity pool | Cluster of resting stop-orders above swing highs / below swing lows or at equal highs/lows |
| Liquidity sweep | Price wicks through a pool then closes back inside — stops triggered, smart money reverses |
| Order Block (OB) | Last opposite-color candle before a strong displacement move |
| Breaker Block | An OB that failed to hold and now acts as resistance/support from the other side |
| Mitigation Block | A zone where price returns to "mitigate" an unfilled order before continuing |
| FVG / Imbalance | 3-candle pattern where candle 1 high < candle 3 low (bullish) — gap between |
| iFVG | An FVG that price returned to and FAILED to respect — gap inverts polarity |
| BPR | Overlap of bullish and bearish FVGs — strong S/R |
| OTE | Optimal Trade Entry: 0.62-0.79 fib retracement of a swing leg |
| Power of Three | Accumulation → Manipulation → Distribution — daily candle anatomy |
| Displacement | Sharp impulsive move that creates an FVG and breaks structure |
| Killzone | High-probability time window — institutional liquidity concentrated |

## Killzones (canonical ICT, EST = UTC-5 in standard, UTC-4 in DST)

| Window | EST | UTC (DST) | IST (UTC+5:30) |
|---|---|---|---|
| Asia | 8 PM – 12 AM | 00:00 – 04:00 | 05:30 – 09:30 |
| London Open | 2 AM – 5 AM | 06:00 – 09:00 | 11:30 – 14:30 |
| NY AM | 8:30 AM – 11 AM | 12:30 – 15:00 | 18:00 – 20:30 |
| NY Lunch | 11 AM – 1:30 PM | 15:00 – 17:30 | 20:30 – 23:00 |
| NY PM | 1:30 PM – 4 PM | 17:30 – 20:00 | 23:00 – 01:30 |
| London Close | 10 AM – 12 PM | 14:00 – 16:00 | 19:30 – 21:30 |

Source: [tradeify.co ICT Concepts](https://tradeify.co/post/ict-concepts-for-prop-firm-trading-and-passing-evaluations).

## ICT 2022 Mentorship Model (canonical workflow)

1. Daily bias from D1/H4
2. Identify HTF liquidity (PD arrays, equal highs/lows, sweep targets)
3. Wait for liquidity sweep / Judas swing
4. Confirm with MSS (impulsive break against the sweep direction)
5. Enter on LTF FVG retest within the displacement leg
6. Target opposite-side liquidity, minimum 1:3 RR

Source: [tradeify.co](https://tradeify.co/post/ict-concepts-for-prop-firm-trading-and-passing-evaluations).

## XAUUSD session behavior (early findings)

- Asian session typically builds a range; London frequently sweeps one side then reverses.
- Asia sweeps tend to **reverse**; London/NY sweeps tend to **continue**.
- Sources: [TradingView Liquidity script](https://tr.tradingview.com/scripts/liquidity/), [Killzone scripts](https://id.tradingview.com/scripts/killzone/), [Sweep script](https://id.tradingview.com/scripts/sweep/).
- *Content rephrased for compliance with licensing restrictions.*

## Statistical reality check

- Public backtests of SMC tools cluster around **45–54% win rate**. Edge comes from RR, not accuracy.
- Sources: [lunetrading order block backtests](https://www.lunetrading.com/blog/best-order-block-indicators-2026-tradingview-top-picks-backtests-win-rates), [TradingView FVG study](https://id.tradingview.com/scripts/fairvaluegaps/).
- Most SMC content is promotional / not statistically rigorous. Critical view: [mindmathmoney](https://www.mindmathmoney.com/articles/ict-trading-concepts-explained-the-truth-without-the-hype) notes ICT concepts are largely repackagings of Dow Theory, Wyckoff, classic S&R.
- *Content rephrased for compliance with licensing restrictions.*

## iFVG specifics (relevant to user's playbook)

- An FVG that price re-enters and **fails to hold** inverts polarity — failed support → resistance.
- Used as reversal/continuation trigger, especially after a liquidity sweep.
- Sources: [fluxcharts](https://www.fluxcharts.com/articles/inversion-fair-value-gaps-ifvg-explained), [mql5](https://www.mql5.com/en/articles/16659), [tradezella IFVG model](https://www.tradezella.com/strategies/ifvg-trading-model).

## Open questions for deep research

1. Strict objective definition of "iFVG inverted" vs. "FVG just consumed" — when does the polarity flip become valid?
2. Statistical edge of liquidity-grab + iFVG combo on XAUUSD specifically (any sample > 100 trades?).
3. Is late-Asia / pre-London XAUUSD a tradeable window or noise?
4. How to score HTF/LTF alignment objectively (currently subjective).
5. Stop placement rules — typical XAUUSD stop-hunt depth in points by session.

The deep-research prompts in `research-prompts.md` are designed to answer these.
