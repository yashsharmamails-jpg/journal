# Trading Journal & Performance Analytics

Personal AI-assisted trading journal. Every trade is stored as a structured
markdown entry, plus a row in a CSV ledger for statistical analysis.

## How to use

1. Send a message: "Here is a trade I took" + screenshots + context.
2. The agent will:
   - Extract pair, timeframe, entry, SL, TP, direction, structure.
   - Compare BEFORE / DURING / AFTER screenshots.
   - Create a new file under `trades/<TRADE_ID>.md` using `templates/trade_template.md`.
   - Append a row to `analytics/ledger.csv`.
   - Update `analytics/performance.md` with rolling metrics.
   - Log new mistakes / patterns in `coaching/lessons.md`.

## Trade ID convention

`YYYYMMDD-<PAIR>-<NN>` — e.g. `20260527-XAUUSD-01` for the first XAUUSD trade
on 27 May 2026.

## Screenshot organization

```
screenshots/<TRADE_ID>/
  before/   # pre-entry charts (the thesis)
  during/   # management updates
  after/    # outcome / post-mortem
```

Within each phase, name files by timeframe: `1m.png`, `5m.png`, `15m.png`,
`1h.png`, `4h.png`, `1d.png`.

## Files

- `trades/`        — one rich markdown entry per trade
- `analytics/ledger.csv` — flat data for stats (win rate, RR, expectancy, etc.)
- `analytics/performance.md` — human-readable rolling report
- `coaching/lessons.md` — pattern log: mistakes, edge, psychology
- `templates/trade_template.md` — schema used for every trade entry
