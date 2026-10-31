---
title: Commodities for the Long Run (AQR, 1877–2015)
type: reference
updated: 2026-10-31
sources: [levine-ooi-richardson-2016-nber-w22793, levine-ooi-richardson-sasseville-2018-faj, faj-2018-abstract-cfa-rpc, aqr-commodities-long-run-data-monthly, aqr-commodities-long-run-data-original]
confidence: medium
tags: [regimes, commodities, inflation, carry, backwardation, datasets]
---

# Commodities for the Long Run (AQR, 1877–2015)

## Contents

- [The two versions](#the-two-versions)
- [The long-run record (equal-weighted commodity futures index)](#the-long-run-record-equal-weighted-commodity-futures-index)
- [State-conditional returns (equal-weighted index)](#state-conditional-returns-equal-weighted-index)
- [Where it lands in the old debate](#where-it-lands-in-the-old-debate)
- [Portfolio conclusions the paper draws](#portfolio-conclusions-the-paper-draws)
- [How their index was built (only what matters for a rebuild)](#how-their-index-was-built-only-what-matters-for-a-rebuild)
- [The public dataset and why it matters](#the-public-dataset-and-why-it-matters)
- [How this connects to our quadrant pages](#how-this-connects-to-our-quadrant-pages)
- [Known gaps](#known-gaps)
- [See also](#see-also)

Short answer: the 139-year record says commodity futures earn a positive
premium, and that the premium lives in **high-inflation, expanding,
backwardated markets** — but it is **not** an equity-like premium ("The
evidence does not, however, support equity-like returns for commodities"),
and over the full period carry, not spot price moves, has been the bigger
piece ("adjusted carry yields (roll yields plus short rates) are a larger
contributor to average futures returns than are excess-of-cash spot
returns, much of it coming from short rates"). The sharpest practical
point: **the backwardation premium is carry; the inflation premium is
spot.** Two different engines wearing the same shirt.

*(confidence: medium — one peer-reviewed study plus its own dataset; no
independent replication in our sources. The dataset section below ("The public dataset and why it matters")
is confidence: high — we verified it directly.)*

## The two versions

| | Working paper | Published article |
| --- | --- | --- |
| Title | Commodities for the Long Run | Commodities for the Long Run |
| Authors | Ari Levine, Yao Hua Ooi, Matthew Richardson | same **plus Caroline Sasseville** |
| Where | NBER Working Paper 22793, November 2016 | Financial Analysts Journal, vol 74(2), pages 55-68 |
| Date shown | November 2016 | CFA Institute page: 2 April 2018 · AQR page: April 30, 2018 |
| Text we read | full PDF (40 pp), fetched 2026-10-31 | **abstract only** — the publisher page blocked automated access (HTTP 403) |

Everything about the paper's content on this page comes from the 2016
working paper text, or from the published abstract as relayed by the CFA
Institute Research and Policy Center page and AQR's own research page. The
published full text is paywalled, so any numbers or new material added
between working paper and journal version are **not** captured here.

The published abstract's own framing of the state result (verified in both
relay copies): "commodity returns in different economic states (inflation
up/down, expansion/recession) vary mostly as a result of moves in the
underlying spot price."

*Quote-retrieval note:* the paper's text here came from a PDF-to-text
extraction with two quirks. It occasionally splits a word ("commodit y",
"14. 8%"), and it splices footnotes into the middle of body sentences — so
the quote in "Where it lands in the old debate" ("commodity futures are
exposed to aggregate states…") is continuous in the paper but broken in
the dump. If a quoted phrase won't grep, retry with a space-tolerant
pattern and a shortened fragment before calling it a misquote.

## The long-run record (equal-weighted commodity futures index)

Returns are read as excess returns: "Since futures require no up-front
capital, one can view the returns on the commodity indices as excess
returns."

| Window | Index mean | Vol | Notes (as reported) |
| --- | --- | --- | --- |
| 1877–2015 | 4.8% | 17.6% | excess spot 2.1% vs adjusted carry 3.9%; "spot return volatility is 18.2% versus adjusted carry volatility of 5.5%" |
| 1877–1945 | 3.8% | 20.8% | carry 3.2%; geometric mean 1.7% |
| 1946–2015 | 5.8% | 13.9% | carry 4.5%; geometric mean 4.9% |
| Benchmarks 1877–2015 | stocks 6.7% (vol 17.0%) · long-term govt bonds 1.1% (vol 5.5%) | — | stocks and bonds are stated as excess returns too |

On the equal **risk**-weighted index, the same split by era: excess spot
returns "2.4% and 1.6%" with adjusted carry "2.8% and 4.4%" for the two
subsamples — i.e. the spot piece shrank and the carry piece grew.

**Read carefully:** the paper's headline mean and its two component means
do not add up (4.8% vs 2.1% + 3.9%). The paper flags the reason in general
terms — "because the log portfolio return is not a weighted sum of the log
individual commodity returns, equation (2) no longer strictly holds." Treat
the components as separately reported pieces, not as a sum to reconcile
against.

## State-conditional returns (equal-weighted index)

| State | Mean return | Driven by |
| --- | --- | --- |
| Backwardation vs contango | 7.7% vs 2.1% | **carry**: adjusted carry 12.2% vs −3.6%; excess spot is actually *lower* in backwardation (−2.9% vs 6.5%) |
| High vs low inflation | 14.8% vs −4.7% | **spot**: 10.4% vs −5.8%; carry barely differs (5.5% vs 2.3%); "volatility of the index returns is essentially the same in these two states" |
| Expansion vs recession | 9.4% vs −7.4% | **spot**: 6.3% vs −9.0%; carry similar (4.3% vs 2.9%); equity beta 0.23 in both states |

The same three splits on the equal **risk**-weighted index, from the
introduction: "earn 7.9% versus 1.5% in periods of backwardation versus
contango; 14.1% versus −4.5% in high inflation versus low inflation cycles;
and 8.9% versus −7.3% in expansions versus recessions."

Diversification and how much the states actually explain:
"Commodity index returns are somewhat predictable at 1-month horizons, and
less so at 1-year and 5-year horizons using investment styles of carry,
value and momentum." In the monthly multivariate regression on business
cycle, carry and inflation, the "R-squared is a reasonable 8.0%" — the
states tilt the odds, they don't predict month-to-month.

## Where it lands in the old debate

- Against Gorton–Rouwenhorst / Bhardwaj–Gorton–Rouwenhorst: the paper is
  "generally supportive" on the mechanism — "commodity futures are exposed
  to aggregate states with a large source of their return variation
  explained by commodity spot returns," summarized as commodity futures
  being "a play on commodity prices".
- Against their headline claim: "The evidence does not, however, support
  equity-like returns for commodities."
- With Erb–Harvey: carry (roll plus the short rate) has been the bigger
  contributor, "much of it coming from short rates" — i.e. a chunk of what
  looked like a commodity premium was interest-rate exposure.

## Portfolio conclusions the paper draws

- Full-sample ex post optimal mean-variance mix: "17% to commodities, 29%
  to stocks and 54% to government bonds."
- "a 54%/36%/10% portfolio of stocks, bonds and commodities consistently
  outperforms a 60%/40% allocation of just stocks and bonds" — over seven
  independent 20-year windows from 1877 through 2015, "the 54/36/10
  portfolio outperforms 60/40 in 4 of the 7 cases".
- Full-sample Sharpe ratios: optimal 0.48, equal-weighted 0.45, 60/40 0.42,
  54/36/10 0.45.
- In high-inflation states "a portfolio 100% in commodity futures has the
  highest Sharpe ratio, i.e., 0.84"; in low-inflation states that flips
  and commodity futures' Sharpe goes negative — the paper's Sharpe passage
  reads "In low inflation states, the opposite is true, with commodity
  futures earning −0.27".

Caveat the paper itself raises on investability: Erb–Harvey's objection is
that "equal-weighted commodity indices are not investable at large size
because too much weight is placed on fringe commodities"; the authors
answer that their aim is "less on whether an index is investable and more
about describing the risk/return properties of the average commodity."
Any live version of this is a different, smaller animal.

## How their index was built (only what matters for a rebuild)

- Price history: "Daily high and low prices for multiple contract
  expirations on several commodity futures are available starting January
  2nd, 1877." Sources: CBOT's *Annual Report of the Trade and Commerce of
  the Chicago Board of Trade* to 1951, Commodity Systems Inc after 1951
  and before 2012, Bloomberg after 2012; rolled return series from S&P,
  Goldman Sachs and Bloomberg for base metals and platinum.
- Early-sample limitation: closing prices weren't recorded, so "the
  analysis uses high and low values, and, in particular, the average of
  these high and low values for the daily return series before closing
  price is available"; early volatility uses the Parkinson range
  estimator.
- Membership: the 1877 start is "corn, wheat, oats, lard, short ribs and
  pork", with cotton, soybeans, soymeal and soyoil "added at various
  points during the 1920s-50s"; "prior to 1945, seven commodities enter
  the sample." The early index is mostly ags and meats — a different asset
  from today's energy-heavy mix.
- Roll rule: monthly, "we hold the nearest of the contracts whose delivery
  month is at least two months away" (Brent oil: three months), splicing
  returns on roll dates, falling back through up to five contracts if the
  desired one has no print. Chosen "to coincide with the procedure
  employed by the popular Goldman Sachs Commodity Index."
- Weighting: equal-weighted, and equal **risk**-weighted (each commodity
  weighted by the inverse of its past-year volatility). Results are
  reported as nearly identical between the two.

## The public dataset and why it matters

AQR publishes two files, both described as index-level data for the two
portfolios it ships (an equal-weighted portfolio and "a long–short
portfolio based on the backwardation/contango of individual commodities").

| File | Page date shown | Coverage |
| --- | --- | --- |
| Commodities for the Long Run: Original Paper Data | October 3, 2018 | "monthly index level data through December 2015" |
| Commodities for the Long Run: Index Level Data, Monthly | May 30, 2025 | "an updated version of the data set used in the paper. We provide monthly index level data and update the data monthly." |

**Verified by us on 2026-10-31** *(confidence: high — primary inspection
of the live file plus its server timestamp)*:

- The live monthly file's last data row is **2025-05-30**. Its
  `Last-Modified` header is `Sat, 21 Jun 2025` and repeats on a
  cache-busting request, so this is not a stale copy served from a proxy.
- The file holds **1,780 monthly rows, 1877-02-28 to 2025-05-30, no gaps
  and no duplicate months** — a clean panel, if you trust AQR's
  construction.
- Internet Archive copies of the dataset page from 2025-09-14, 2026-02-09
  and 2026-05-11 all still display "May 30, 2025".
- Control test, same day: AQR's *Momentum Indices, Monthly* file reports
  `Last-Modified: Mon, 05 Oct 2026` with the page showing September 30,
  2026 data. AQR is still maintaining other datasets — this one has just
  gone quiet, ~17 months past its last update.

Practical consequence: **May 2025 is the hard end of the usable public
sample.** Anything later needs our own futures data.

Gotchas in the file, all observed directly:

- It is **index-level only** — 11 columns (equal-weight excess return,
  excess spot, adjusted carry, spot, carry; the same three for the
  long/short portfolio; aggregate backwardation/contango level; state of
  backwardation/contango; state of inflation). The per-commodity daily
  futures prices behind the paper are not published, so the portfolios
  cannot be rebuilt from this file, only compared against.
- The date column is stored as **text** for the first 275 rows (through
  December 1899) and as **date serial numbers** after that; a naive import
  mixes the two.
- The last row (May 2025) has **State of inflation blank**.
- The "Definition" and "Data Sources" tabs are **pasted images**, not text
  — the state definitions are not machine-readable, so state flags can't
  be audited from the file alone.

## How this connects to our quadrant pages

The paper's state table is an inflation × growth × curve-shape grid, so it
reads as the long-run evidence behind the same four quadrants our
[asset performance page](asset-performance-by-quadrant.md) tabulates (that
page lists commodities as favored in reflation and commodity-linked assets
in stagflation). The two agree directionally, and AQR's numbers say *why*
commodities work in the hot quadrants: the inflation premium comes through
spot prices. But the mechanism split adds something our quadrant pages
don't carry: a curve-shape tilt pays for a *different* reason, and would
not be doing the same job in a stagflation allocation.

## Known gaps

- Published (2018 journal) full text is paywalled; the working paper is
  what we hold. If the journal version changed numbers or added exhibits,
  we don't know.
- No independent replication in our sources — every number here is from
  one research team, and two of the three working-paper authors were at
  AQR, a firm that "offers financial products that invest in commodities."
- No state definitions in machine-readable form, and no per-commodity data.
- The paper's own caution that states of nature overlap: "there may be
  correlation between the states of nature that lead to an omitted
  variables problem," with the note that average inflation in recessions
  versus expansions was −1.27% versus 3.63% — so the "growth" and
  "inflation" splits are not cleanly separable.
- No commodity data after May 2025 from this source.

## See also

- [Asset Performance by Growth × Inflation Quadrant](asset-performance-by-quadrant.md) — the quadrant table this evidence backs, and Man Group's regime tests
- [The Growth × Inflation Four-Quadrant Framework](growth-inflation-quadrants.md) — the state definitions the paper's inflation/growth flags roughly match
- [When Bonds Fail, What To Own Instead](when-bonds-fail.md) — the inflation quadrants through the bond lens; commodities as the alternative shield
- [Long-Horizon Stock & Bond Datasets for the 60/40 Legs (U.S., 1871–Present)](long-horizon-stock-bond-datasets.md) — the verified stock/bond pairing for backtests on this basket
