# Coaching Log

Running record of behavioral, technical, and psychological patterns.
Updated after every trade.

## Recurring mistakes

| Mistake | Count | Last seen | Cost (R) | Notes |
|---------|-------|-----------|----------|-------|
| No before screenshot | 1 | 2026-05-27 | 0R | Did not affect this trade's outcome but blocks future audit |
| Stop buffer too tight (XAUUSD <15pt) | 1 | 2026-05-27 | 0R | Won by luck. Will lose money on next sequence if not fixed |
| BE moved before secondary 15m structure break | 1 | 2026-05-27 | 0R | Did not affect this trade because TP filled |
| Account size / risk % undocumented | 1 | 2026-05-27 | n/a | Blocks % risk tracking |

## Recurring strengths

| Strength | Count | Last seen |
|----------|-------|-----------|
| HTF/LTF SMC alignment (15m liquidity → 1m iFVG) | 1 | 2026-05-27 |
| Clean TP placement at prior 15m structure | 1 | 2026-05-27 |
| Disciplined disengagement after BE (no over-management) | 1 | 2026-05-27 |
| Setup choice in highest-evidence tier of SMC playbook | 1 | 2026-05-27 |

## Psychology patterns

- FOMO entries: 0
- Revenge trades: 0
- Fear-based exits: 0
- Overtrading days: 0
- Patience wins: 1 (waited for HTF sweep before 1m execution)

## Edge hypothesis

_(needs ≥ 20 trades to be statistically meaningful)_

- Current hypothesis: liquidity grab + iFVG on XAUUSD 15m/1m has statistical
  basis in the literature (Osler stop-cascades, Cont OFI), but published
  win-rate claims (~70%) come from anecdotal samples ≤60 trades. Build own
  sample to validate.
- Confirming evidence: N=1 trade, 7.25/10 rubric, +2.74R. Insufficient.
- Disconfirming evidence: none yet.

## Open improvement targets (in priority order)

1. **Capture before screenshots — no exceptions.** 15m + 1m, with annotations,
   *before* clicking buy/sell. This is process-level zero-tolerance.
2. **Apply 15–20 pt minimum stop buffer on XAUUSD.** Stop buffer below 15 pts
   on Gold = trade not taken.
3. **Document Asian range size.** If trading the late-Asia window, range must
   be ≥40 pts top-to-bottom.
4. **Log account size on every trade** so risk % is tracked.
5. **Move sessions when possible.** Late-Asia (10:00–14:00 IST) is moderate-edge.
   London Open (12:30–15:30 IST) and NY AM (17:30–20:30 IST) are higher-edge.
6. **BE rule:** only move SL to BE after a secondary 15m structure breaks in
   trade direction. Not at 1:1 in profit.

## Reference docs

- `knowledge/01-ict-smc-reference.md` — concept definitions
- `knowledge/02-edge-evidence.md` — what the data actually says
- `knowledge/03-xauusd-playbook.md` — your specific workflow + scoring rubric
