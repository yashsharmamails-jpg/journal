# Deep-Research Prompts

These are prompts to feed into Gemini Deep Research, Perplexity Pro, and
ChatGPT (Deep Research mode). The outputs are then synthesized into the
knowledge files in this folder.

Run each prompt on at least 2 of the 3 tools so we can cross-reference
disagreements between LLMs.

---

## Prompt 1 — ICT/SMC Concept Reference (objective rules)

Output target: `knowledge/01-ict-smc-reference.md`

```
You are producing a reference document for an active SMC/ICT trader on XAUUSD
who trades multi-timeframe (15m HTF context, 1m execution) and needs strict,
objective identification rules to remove hindsight bias from his pattern
recognition.

For EACH of the following concepts, produce: (a) a one-paragraph definition,
(b) a strict bullet-list of OBJECTIVE rules to identify the pattern in real
time (numeric/structural where possible), (c) common false-positive failure
modes, (d) the highest-probability use case (which timeframe, which session,
which market state), and (e) at least one contrarian view from credible
critics.

Concepts to cover:
1. Break of Structure (BOS)
2. Change of Character (CHoCH)
3. Market Structure Shift (MSS) — and how it differs from BOS/CHoCH
4. Liquidity pools (buy-side, sell-side, equal highs/lows, trendline liquidity)
5. Liquidity sweep / stop hunt / Judas swing
6. Order Block (bullish, bearish) — strict 3-criteria definition
7. Breaker Block
8. Mitigation Block
9. Fair Value Gap (FVG / Imbalance) — strict definition, lifespan rules
10. Inverse Fair Value Gap (iFVG) — exactly when an FVG inverts vs. is just consumed
11. Balanced Price Range (BPR)
12. Premium / Discount and Optimal Trade Entry (OTE) — including fib levels
13. Power of Three (Accumulation / Manipulation / Distribution)
14. Displacement and how to measure it objectively
15. Killzones (London Open, NY AM, NY Lunch, NY PM, Asia, London Close) with
    exact UTC and EST times
16. Silver Bullet (the 1-hr window models)
17. Daily bias derivation method (D1, H4, H1 hierarchy)
18. ICT 2022 Mentorship Model — full step-by-step
19. ICT 2024 Model (any updates, if any)
20. SMT divergence (correlated pairs)

Format: Markdown, with each concept as an H2 section and the (a)-(e)
sub-sections as H3. Use tables for time windows. Cite sources inline with
markdown links (prefer original ICT material, then peer-reviewed critique,
then well-trafficked educational sites; avoid promotional broker content).

Length target: 4000-6000 words. Be precise. No hype. No motivational language.
```

---

## Prompt 2 — Statistical Edge & Backtest Evidence

Output target: `knowledge/02-edge-evidence.md`

```
You are producing an evidence file for a discretionary SMC/ICT trader who
wants to know WHICH SMC concepts have measurable statistical edge and which
are cherry-picked / hindsight-biased.

Find and synthesize:
1. Every publicly available backtest of SMC/ICT concepts you can locate
   (academic papers, GitHub repos, prop-firm internal studies leaked publicly,
   TradingView script backtests, Substack / Medium quant write-ups).
2. For each study, report: concept tested, instrument(s), timeframe,
   sample size (number of trades), win rate, average RR, profit factor,
   max drawdown, expectancy in R, time period covered, methodology
   transparency (1-5), source URL.
3. Critically note any study where: sample size < 100, methodology is opaque,
   selection bias is likely, or the study is clearly marketing.
4. Identify the 3 SMC concepts with the STRONGEST evidence base, and the 3
   with the WEAKEST / most subjective.
5. List the top failure modes documented across studies (e.g. "FVGs in
   ranging markets fail X% of the time").
6. Identify any peer-reviewed academic literature on order flow, liquidity
   provision, or stop-hunt phenomena that LEND or REMOVE credibility from
   SMC claims.

Specific instruments of interest: XAUUSD (gold), EURUSD, NAS100, BTCUSD.
Specific concepts of highest interest: liquidity grab + iFVG, liquidity grab
+ OB, OTE entries on H1/M15.

Format: Markdown.
- Section 1: Summary table (concept | studies found | median win rate |
  median RR | confidence rating)
- Section 2: Detailed study-by-study breakdown
- Section 3: What the evidence supports vs. doesn't
- Section 4: Recommended journaling fields to validate edge personally

Be skeptical. Flag promotional content. Cite every claim with a URL.
Length target: 3000-5000 words.
```

---

## Prompt 3 — XAUUSD Session Behavior + Multi-TF Execution Playbook

Output target: `knowledge/03-xauusd-playbook.md`

```
You are producing a session-and-instrument-specific playbook for a discretionary
SMC trader who trades XAUUSD primarily on 15m (HTF context) and 1m (execution),
with the trade workflow: identify HTF liquidity → wait for sweep → enter on
LTF iFVG rejection + BOS.

Cover:

1. XAUUSD micro-structure by session (with exact UTC times and IST conversions
   since the trader is in India, UTC+5:30):
   - Sydney/Tokyo (Asia) — typical range, average ATR, typical behavior
   - Frankfurt/London pre-open
   - London open killzone
   - London-NY overlap
   - NY AM killzone
   - NY PM
   - London close
   For each: average daily range contribution, sweep behavior, reversal vs.
   continuation tendency, liquidity that typically gets taken, common traps.

2. Asia-session XAUUSD specifically: documented behavior of late-Asia /
   pre-London moves (the trader's window). Is this window high-edge or
   low-edge for SMC traders? What conditions make it tradeable vs. avoid?

3. The 15m → 1m execution model:
   - How to derive 15m bias correctly
   - When 1m signals should override 15m vs. defer to 15m
   - iFVG on 1m: typical lifespan, invalidation rules, expected RR
   - BOS on 1m as confirmation: how to distinguish real BOS from noise
   - Stop placement best practices for 1m entries on XAUUSD
     (spread, slippage, typical stop-hunt depth in points)

4. Common psychological pitfalls specific to this style:
   - Over-identifying iFVGs in ranging markets
   - Forcing setups in low-volume Asia
   - BE-and-walk-away vs. trail-stop trade-offs
   - Greed extension past HTF supply

5. A scoring rubric (0-10) for grading any individual SMC trade post-hoc on:
   HTF alignment, liquidity quality, entry trigger quality, stop placement,
   target placement, management, journaling completeness.

Format: Markdown with tables for session times and behavior. Specify all
times in BOTH UTC and IST. Cite sources.
Length target: 3000-4500 words.
```

---

## How to deliver

For each prompt:
1. Paste it into Gemini Deep Research / Perplexity Pro / ChatGPT.
2. Save the response. Tag which tool produced it.
3. Send the output back. The agent will synthesize into the corresponding
   `knowledge/0X-*.md` file, flagging disagreements between sources.
