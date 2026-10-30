---
title: The Growth × Inflation Four-Quadrant Framework
type: concept
updated: 2026-10-30
sources: [bridgewater-all-weather-story, four-quadrants-gave-framework, resolve-structural-diversification, man-regime-based-investing, swoopr-growth-inflation-quadrants]
confidence: medium
tags: [regimes, macro, framework]
---

# The Growth × Inflation Four-Quadrant Framework

## Contents

- [The idea](#the-idea)
- [The four quadrants and their names](#the-four-quadrants-and-their-names)
- [Where it came from](#where-it-came-from)
- [The key definitional question: levels vs surprises](#the-key-definitional-question-levels-vs-surprises)
- [Detecting the current quadrant](#detecting-the-current-quadrant)
- [How to use it](#how-to-use-it)
- [See also](#see-also)

## The idea

Most macro risk can be decomposed into two dimensions: the **direction of
real economic growth** (rising or falling) and the **direction of
inflation** (rising or falling). Crossing them gives four regimes — the
"quadrants." Each quadrant has historically produced distinct relative
performance across asset classes: no single asset wins in all four, so
knowing the quadrant tells you which assets are relatively favored
(*confidence: medium* — all five sources agree directionally; per-asset
claims vary, see [asset-performance-by-quadrant](asset-performance-by-quadrant.md)).

The framework is most useful not as a prediction tool but as a mapping
tool: it tells you which quadrant each asset in your portfolio is
exposed to, and therefore where you're structurally weak to regime
shift (ReSolve notes the traditional 60/40 is essentially suited to
only *one* of the four regimes — disinflationary boom).

## The four quadrants and their names

Naming varies by source; the map below reconciles them.

| Growth | Inflation | Common name | Gavekal name | Era example (as cited in our sources) |
| --- | --- | --- | --- | --- |
| Rising | Falling | **Goldilocks** | Deflationary boom | 1981–2000 (ReSolve: disinflationary growth period) |
| Rising | Rising | **Reflation** | Inflationary boom | 2003–mid 2008 (ReSolve) |
| Falling | Rising | **Stagflation** | Inflationary bust | *(none cited in our sources)* |
| Falling | Falling | **Deflation** / bust | Deflationary bust | Great Depression (ReSolve) |

- Man Group splits each axis into four states instead of two
  (e.g. inflation: FIRE, REFLATION, DISINFLATION, ICE; growth:
  BOOM, RECOVERY, SLUMP, RECESSION with NBER recessions as baseline).
- Bridgewater (Dalio) insists the axes are about **surprises relative
  to what's priced in**, not raw direction — see below.

### Correction 2026-10-30 (same-day QA): era examples were unsourced

The first version of the table listed "1973–75, 2022" (stagflation) and
"2008 crisis" (deflation) as era examples, and called Goldilocks's
Gavekal name "Disinflationary boom." Neither holds up against the
registered sources: the specific era examples appear in **none** of the
five articles (plausible, but unciteable — era windows matter if we ever
test a detector, so they shouldn't be invented), and the
disinflationary-boom term is **ReSolve's**; our registered Gave-relaying
source (portfoliooptimizer.io) writes "Deflationary Boom." The era
column now lists only eras the sources actually name.

## Where it came from

- **Charles Gave** — worked out the "four quadrants" in **1978**
  (per Gavekal's own account, relayed by portfoliooptimizer.io). His
  version is the *Growth and Inflation Matrix*, elaborated in his 2024
  book *The General Theory of Portfolio Construction*.
- **Harry Browne** — the Permanent Portfolio (launched 1982;
  *Fail-Safe Investing*, 1999) popularized the four-quadrant framing:
  25% each in stocks, long bonds, cash, gold — one asset per regime.
- **Ray Dalio / Bridgewater** — All Weather (created 1996), the
  foundation of "risk parity": balance risk across assets by how they
  respond to the four growth/inflation *environments*
  ([The All Weather Story](https://www.bridgewater.com/resources/all-weather-story.pdf)).

## The key definitional question: levels vs surprises

The sources disagree on what "rising" and "falling" mean, and this
matters for any live detector:

- **Gave / Gavekal, ReSolve, Swoopr**: axes are the *level/direction* of
  growth and inflation (accelerating vs decelerating).
- **Bridgewater**: markets price in expectations, so what moves prices
  is the *gap between actual conditions and priced-in conditions* — a
  "surprise." Markets don't react to growth per se, but to whether
  growth is better/worse than expected.

- **Swoopr's hybrid**: direction relative to *trend or consensus
  expectations* — the absolute level matters less than whether it's
  surprising positively or negatively.

**Open question (unresolved):** for a live quadrant detector, should
the state be measured by raw direction (Gave's ratios do this) or by
expectation gaps (Dalio's principle, harder to operationalize)?
Resolution needed before building any detection rules.

## Detecting the current quadrant

**Gave's rules** (per portfoliooptimizer.io's implementation, from his
2024 book; both vs a 7-year moving average):

- **Energy Efficiency Ratio** = S&P 500 / WTI oil price. Above 1 →
  economy is energy-efficient and growing → top half of the matrix.
- **Currency Debasement Ratio** = total return of 10-year
  constant-duration Treasuries / gold price. Above 1 → bonds are a
  proper store of value, inflation contained → bottom half.

Gave's reasoning: equities vs oil captures productive use of energy;
bonds vs gold captures whether paper money holds its value.

**Indicator-based approach** (Swoopr): leading growth indicators —
ISM PMI, Conference Board LEI, jobless claims, yield-curve slope;
inflation indicators — CPI/PCE trend, breakeven inflation rates,
commodity prices (lead headline CPI by ~3–6 months), wage growth; plus
market cross-checks — credit spreads, cyclical-vs-defensive sector
performance.

**Caveats**: Man Group's empirical treatment(*The Road Ahead*, May 2026)
is the useful skeptic: all regime frameworks are "messy" — signals work
directionally but not definitively; regimes are clearer in hindsight
than in real time. Swoopr's practical advice: operate with
probabilities over quadrants rather than binary calls; tilt 5–15
percentage points, not wholesale rotations.

## How to use it

1. **Structural diversification** (ReSolve, Browne, Bridgewater): don't
   bet on the quadrant — hold assets that cover all four, weighted so
   the portfolio is balanced across regimes. What varies is *how* you
   weight (equal capital → Permanent Portfolio; risk-balanced → All
   Weather / risk parity).
2. **Macro overlay** (Swoopr): small tilts toward the
   historically-favored assets of the current quadrant, multiple
   indicator confirmations before changing the call.
3. **Empirical caution** (Man Group): if forced to pick one economic
   data series, US headline CPI; commodity-based and inflation-based
   regime states showed the most persistent signals in their tests.

## See also

- [Asset performance by quadrant](asset-performance-by-quadrant.md) —
  which assets win where, with per-claim attribution and Man Group's empirical findings
- [When Bonds Fail, What To Own Instead](when-bonds-fail.md) —
  synthesis: the inflation quadrants through the bond lens
