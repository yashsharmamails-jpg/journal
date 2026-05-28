# Coaching Log

Running record of behavioral, technical, and psychological patterns.
Last update: 2026-05-27 (Trade 03).

## Recurring mistakes

| Mistake | Count | Last seen | Cost (R) | Notes |
|---------|-------|-----------|----------|-------|
| No liquidity sweep before entry | 2 | 2026-05-27 T03 | -1.14R / +1.72R | Model precondition violated |
| CHoCH used instead of MSS | 2 | 2026-05-27 T03 | mixed | **Trader doesn't know MSS** |
| FOMO entry (zone without trigger) | 1 | 2026-05-27 T02 | -1.14R | |
| Shorted into liquidation flow | 1 | 2026-05-27 T02 | -1.14R | "sellers stopped out" above entry |
| SL buffer too tight (XAUUSD <15pt) | 3 | 2026-05-27 T03 | 0R direct | Won 2/3 by luck |
| **Trade after "done for the day"** | 1 | 2026-05-27 T03 | +1.72R | **DISCIPLINE VIOLATION** |
| Trading off-killzone | 1 | 2026-05-27 T03 | 0R | 22:47 IST = dead zone |
| Numbers typed don't match chart | 1 | 2026-05-27 T03 | 0R | Verify broker in AM |
| No before screenshot | 2 | 2026-05-27 T02 | 0R | Fixed on T03 |
| BE moved before secondary 15m break | 1 | 2026-05-27 T01 | 0R | |

## Recurring strengths

| Strength | Count | Last seen |
|----------|-------|-----------|
| HTF/LTF SMC alignment (sweep + iFVG) | 1 | 2026-05-27 T01 |
| Correct zone ID | 3 | 2026-05-27 T03 |
| Clean TP placement | 3 | 2026-05-27 T03 |
| Disciplined risk sizing (<0.5%) | 3 | 2026-05-27 T03 |
| Healthy post-loss psychology | 1 | 2026-05-27 T02 |
| Disciplined disengagement | 2 | 2026-05-27 T03 |
| **Before screenshots taken** | 1 | 2026-05-27 T03 (FIRST TIME) |

## Psychology patterns

- FOMO entries: 1 (T02)
- Revenge trades: 0 explicit, **1 likely** (T03 — same energy after "done for the day")
- Fear-based exits: 0
- Overtrading days: **1** (T03 violated "done for the day")
- Patience wins: 1 (T01)
- **Lucky-win blindness:** T03 won money but failed process (4.0/10). Risk: feeling good about a win regardless of process.

## The #1 lesson from Day 1

> **Zone ≠ Trigger. CHoCH ≠ MSS.**
>
> Step 1: HTF zone — done correctly on all 3 trades.
> Step 2: 1m **MSS with displacement** — only on T01.
> Step 3: iFVG retest — only on T01.
>
> T01: Steps 1-2-3 → WIN +2.74R, rubric 7.25
> T02: Step 1 only → LOSS -1.14R, rubric 6.0
> T03: Step 1 only → WIN +1.72R, rubric 4.0 (lucky)
>
> **The skill gap is MSS recognition, not zone identification.**

## CRITICAL Knowledge gap

**Trader does not know what MSS is.** Confirmed on T03.

Per `knowledge/01-ict-smc-reference.md`:

> **MSS strict rule (all 3 must be true):**
> 1. Liquidity sweep occurred first
> 2. Body close beyond opposing structural swing
> 3. Displacement: ≥2× ATR(20), body ≥80% of range, leaves FVG
>
> **CHoCH ≠ MSS.** CHoCH = warning. MSS = CHoCH + displacement.

**Action:** read sections 2 and 3 of knowledge/01-ict-smc-reference.md before any trade.

## Edge hypothesis (refined)

- **Refined (N=3):** sweep + MSS + iFVG has edge. Without sweep AND without MSS = coin flip (1W/1L on N=2 of those).
- T01 (full process) → +2.74R confirms.
- T02 & T03 (no sweep, no MSS) → +0.29R avg with rubric 5.0/10. Wins are luck.

## Open improvement targets (priority)

1. **LEARN MSS.** Read knowledge/01-ict-smc-reference.md sections 2 and 3.
2. **WAIT FOR LIQUIDITY SWEEP** before any entry. Skipped on 2/3.
3. **WAIT FOR 1m MSS + DISPLACEMENT.** CHoCH alone isn't enough.
4. **"Done for the day" is inviolable.** Broken once, won by luck. Next time = -3R day.
5. **15-20 pt stop buffer** on XAUUSD.
6. **Track MAE and MFE.**
7. **Prefer London Open / NY AM** killzones.

## Daily log

### 2026-05-27 (Day 1)
- **Trades:** 3
- **Results:** +2.74R, -1.14R, +1.72R = **+3.32R (+$45.80)**
- **Account:** $3,000 → $3,045.80
- **Avg rubric:** 5.75/10 (declining: 7.25 → 6.0 → 4.0)
- **Key knowledge gap:** MSS — must learn before next session
- **Discipline:** Broken (T03 after "done for the day")
- **Improvement:** Before screenshots captured for the first time (T03)

## What "good Day 2" looks like

1. Read knowledge/01-ict-smc-reference.md sections 2, 3, 14 (MSS, CHoCH, displacement).
2. Re-read knowledge/03-xauusd-playbook.md workflow.
3. Verify T03 actual fill prices from broker statement.
4. Skip any setup without:
   - Liquidity sweep before entry
   - 1m MSS with displacement (NOT CHoCH alone)
   - 15+ pt stop buffer
5. **Honor "done for the day" — no exceptions.**
