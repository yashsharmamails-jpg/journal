# AI-Readable Chart Indicator

A Pine Script v6 indicator that turns any TradingView chart into something a
vision-capable AI (ChatGPT, Claude, Gemini) can actually read and explain.

## What it shows

| Marker | Meaning |
|---|---|
| `C###` | Candle ID = last 3 digits of bar index (e.g. `C244`) |
| `LSH` / `LSL` | Liquidity sweep of swing high / low |
| `EQH` / `EQL` | Sweep of equal highs / equal lows |
| `BOS↑` / `BOS↓` | Break of structure |
| `CHOCH↑` / `CHOCH↓` | Change of character (trend flip) |
| `FVG↑` / `FVG↓` | Fair value gap (with `mit C###` when filled) |
| `OB↑` / `OB↓` | Bullish / bearish order block |
| `DISP` | Displacement candle (large body + range vs ATR) |
| Background tint | Asia (yellow) / London (blue) / NY (green) |
| Top-right table | Plain-text summary of the most recent events |

The summary table is the most reliable thing for the AI to read — labels
on candles can collide at zoomed-out scales, but the table is always clear.

## How to install in TradingView

1. Open any chart on tradingview.com.
2. Bottom panel → **Pine Editor**.
3. Paste the contents of `ai-readable-chart.pine`.
4. Click **Save** (give it any name) → **Add to chart**.
5. Click the gear icon next to the indicator name to tweak settings per
   timeframe / instrument.

## Recommended workflow

1. Set timeframe and instrument (e.g. XAUUSD 5m).
2. Wait for the chart to render. Check the top-right summary table.
3. Take a clean screenshot — full chart, summary table visible, legend
   visible on the right edge.
4. Drop the screenshot into your AI of choice and ask, e.g.:
   - "Which candle swept liquidity and what happened after?"
   - "Did C244 break structure, and is there an unmitigated FVG nearby?"
   - "Is the current price reacting to an order block?"

## Tuning tips

- **1m / 5m charts:** lower `Number every N candles` to 3 and reduce
  `Recent candles to number` to 150 to keep labels readable.
- **Higher timeframes:** raise swing pivot length to 7–10 so BOS / CHOCH
  marks only meaningful swings.
- **Clean screenshots for AI:** turn off TradingView's volume pane, hide
  the watchlist, and use a high-contrast theme. Dark theme works well
  with the current label colors.

## Known limits

- TradingView caps `max_labels_count` at 500. The script numbers only the
  most recent N candles plus all event candles, so it stays under the cap.
- Order block detection is the simplified "last opposite candle before a
  strong move" definition. Refine it if you have a stricter rule.
- All structure / sweep detection runs on `barstate.isconfirmed` — no
  repainting on closed bars, but the current forming bar is not labelled
  until it closes.
