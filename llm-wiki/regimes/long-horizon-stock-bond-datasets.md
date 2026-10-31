---
title: Long-Horizon Stock & Bond Datasets for the 60/40 Legs (U.S., 1871–Present)
type: reference
updated: 2026-10-31
sources: [shiller-online-data, shiller-ie-data-yale-mirror, shiller-ie-data-yale-file, fred-gs10-table, fred-gs10-series, damodaran-histret-1928, measuringworth-datasets, measuringworth-interest-sources, jordà-etal-2019-rroe-nber, rroe-replication-dataverse, jst-macrohistory-db, aqr-commodities-long-run-data-monthly]
confidence: high
tags: [regimes, datasets, equities, bonds, 60-40, backtesting]
---

# Long-Horizon Stock & Bond Datasets for the 60/40 Legs (U.S., 1871–Present)

Short answer: **Robert Shiller's free monthly spreadsheet is the pairing** —
it is the only source we found that carries monthly U.S. stock total
returns **and** a monthly long-bond total-return series from **1871 to the
present**, so it overlaps AQR's monthly commodity index (Feb 1877 – May
2025) row-for-row. The annual academic datasets (Jordà–Schularick–Taylor)
are cross-checks, not drivers; Damodaran's long-return table starts only in
1928 and is annual. The bond leg you get from Shiller is a *synthetic*
10-year Treasury, not a traded bond index — verified below, and it matters.

## Why this page exists

[Commodities for the Long Run (AQR, 1877–2015)](commodities-for-the-long-run.md)
documents a monthly commodity-futures index dataset whose public file ends
May 2025 and has stopped updating. To backtest anything on that basket with
a 60/40 comparison (the AQR paper runs its own 60/40 and 54/36/10 portfolio
exercises), we need monthly U.S. stock and bond return series over the same
window — 1877 to present. This page records what we verified, on
2026-10-31, by downloading the files and reading the source pages.

## The pairing: Shiller's monthly file *(verified by us 2026-10-31; confidence: high — primary inspection)*

Robert Shiller's "Stock Market Data Used in *Irrational Exuberance*" —
downloaded live from shillerdata.com on 2026-10-31 (the download link is a
hosted blob whose URL carries a `?ver=` query string, so resolve it from the
page rather than hard-coding it).

Verified properties of the live file:

- **1,870 consecutive monthly rows, January 1871 through October 2026 —
  no gaps** (our count over the date column).
- The price and interest-rate columns run through October 2026; the
  **"Monthly Total Bond Returns" column through September 2026** (the
  formula needs the *next* month's yield — see the bond section); dividend
  and earnings columns through June 2026, i.e. the tail is provisional.
- Cross-check against the official rate series: the file's September 2026
  10-year rate is **4.99**, and FRED's GS10 series page shows
  "Sep 2026: 4.99" — an exact match.
- The Yale mirror of the file is **stale**: file properties show last
  saved 2023-09-17, and its data ends 2023.09 (1,833 rows) — all verified
  against the mirror file itself, still hosted at
  `econ.yale.edu/~shiller/ie_data.xls` (registered:
  shiller-ie-data-yale-file). Location gotcha: Yale's data page
  (`econ.yale.edu/~shiller/data.htm`) no longer *links* the monthly file —
  its only download today is a different, annual file (1871–2016) — so
  cite the direct file URL, not the page. Use the shillerdata.com copy.
  *(Correction [2026-10-31 review]: this bullet originally credited the
  stale-file facts to the data.htm page; the facts are true — re-verified
  against `ie_data.xls` itself — but the page's linked file is a
  different, newer one, so the citation is re-pointed to the actual
  file.)*

The data page's own description (fetched 2026-10-31): the dataset is
"monthly stock price, dividends, and earnings data and interest rates and
the consumer price index (to allow conversion to real values), starting
January 1871." Construction details stated on the page: "Stock price data
are monthly averages of daily closing prices" (not month-end closes);
post-1926 dividends and earnings are interpolated from "the S&P
four-quarter totals … with linear interpolation to monthly figures";
pre-1926 dividends and earnings are "from Cowles and Associates …
interpolated from annual data"; the CPI is spliced to Warren & Pearson's
price index before 1913.

## The stock leg

The file has no stock *return* column — total returns must be computed from
price + dividends. Our convention (ours, not Shiller's):
`(P + D/12) / P(prev) − 1`, with `D` the annualized dividend rate.

Quick arithmetic-annualized stats from our recomputation of the live file
(monthly mean × 12; a rough check, not a published figure):

| Window | Stock total return | Vol |
| --- | --- | --- |
| 1871–2015 | ≈9.6%/yr | ≈14.1% |
| 1946–2015 | ≈11.0%/yr | ≈12.1% |

Sanity anchor: the AQR paper's benchmarks (1877–2015) are 6.7% stocks in
*excess* terms; a ~9.6% nominal total return minus cash over a slightly
different window is the same ballpark, but note the conventions differ
(see "The cash-leg gap").

## The bond leg is synthetic — verified, not suspected

The "Monthly Total Bond Returns" column is **not** a bond index. We
recomputed it from the file's own long-rate column and matched the reported
values for **all 1,869 populated months (max difference 1.6e-15 — exact to
rounding)**. The formula is:
a bond bought at par at month *t*'s 10-year yield (coupon = that yield),
held one month, and marked at month *t+1*'s yield with 119 months left.

Consequences for a backtest:

- It is a **rolling one-month hold of a ~10-year Treasury** — duration
  exposure, not a traded bond fund. Our stats: ≈4.9%/yr at 4.3% vol
  (1871–2015) and ≈5.8% at 6.1% (1946–2015). Monthly extremes: −8.3% /
  +10.9%. Smooth — intermediate-rate-like, not long-bond-index-like.
- The official rate behind it (FRED GS10, "Market Yield on U.S. Treasury
  Securities at 10-Year Constant Maturity, Quoted on an Investment Basis")
  has FRED-stated "Date Range 1953-04-01 to 2026-09-01." **Shiller's rate column runs from
  1871 — the pre-1953 rates are a stand-in**; the shillerdata.com page
  (read 2026-10-31) does not document how they were made. Treat the
  pre-1953 bond leg as approximate. *(confidence: medium for pre-1953;
  high for 1953+, where the inputs are official.)*

## The cash-leg gap

AQR's commodity series is quoted as **excess returns** (futures need no
up-front capital), while Shiller's stock and bond series are total returns.
Combining them means subtracting a cash rate from every leg or adding it
to none — a bookkeeping decision to lock down **before** any backtest code
exists. Shiller's file carries **no T-bill column** (columns inspected:
only the long rate), so a separate cash series is needed. MeasuringWorth's
interest-rate documentation describes a U.S. short-term series "available
from 1831-present," commercial paper to 1930 and Treasury bills after.
*(Confidence upgraded to high in the 2026-10-31 review: the page was
unfetchable at compile time and this rested on search-result text; the
review session fetched the page directly and the reading matches —
"available from 1831-present," "From 1831-1930, it was in the form of a
commercial paper. From 1931-present, it is in the form of a treasurer
bill." [sic].)*

## Annual cross-check datasets (not backtest drivers)

- **The Rate of Return on Everything, 1870–2015** (Jordà, Knoll, Kuvshinov,
  Schularick & Taylor; NBER w24112; QJE vol 134 issue 3, 2019, pages
  1225–1298). Abstract, verified in the fetched NBER page: "The annual data
  on total returns for equity, housing, bonds, and bills cover 16 advanced
  economies from 1870 to 2015." Replication data is registered at Harvard
  Dataverse ("Replication Data for: 'The Rate of Return on Everything,
  1870-2015'", published 2019-03-26).
- **Jordà–Schularick–Taylor Macrohistory Database** (macrohistory.net).
  Its download page describes release R.6: "the data now covers 18 advanced
  economies since 1870 on an annual basis," including "long-term returns on
  housing, equities, bonds and bills." *(Confidence upgraded to high in the
  2026-10-31 review: the site was unfetchable at compile time and this
  rested on search-result text; the review session fetched the download
  page directly and both quotes matched verbatim.)*

Both are **annual** — right answer for cross-checking a monthly backtest
year by year, wrong shape to drive it. The RRoE paper's window explicitly
ends in 2015 (its abstract says so); the macrohistory download page states
its coverage start ("since 1870") but nowhere states an end year, so the
JST data's own end date is unknown from our sources.
*(Correction [2026-10-31 review]: this passage earlier said "their papers'
windows end in 2015" for both datasets; the 2015 end greps only in the
RRoE abstract, not in any macrohistory page we fetched, so the claim is
scoped to what the sources state.)*

## Other options evaluated

- **Damodaran** (NYU Stern): "Historical Returns on Stocks, Bonds and
  Bills: 1928-2022" — annual U.S. stocks/bonds/bills, page dated January
  2024 (fetched 2026-10-31). Rejected as a pairing: starts 1928 and annual.
- **MeasuringWorth** lists "The Annual Standard and Poor's Composite Stock
  Index for the United States, 1871 to Present" and "Interest Rate Series
  for the United Kingdom and the United States, 1729 to Present" (fetched
  2026-10-31). Useful for the cash leg and cross-checks; annual, so not
  the backtest driver.
- Paid subscription databases: **not evaluated — none cited in our
  sources.**

## If you want X, use Y

| Want | Use | Why |
| --- | --- | --- |
| Monthly stock leg, 1871+ | Shiller file, `(P + D/12)/P − 1` | Only free monthly series this deep |
| Monthly bond leg, 1871+ | Shiller "Monthly Total Bond Returns" | Verified synthetic 10-yr Treasury; know what it is |
| Current months (2025+) | Shiller live file (to Oct 2026 as of 2026-10-31) | AQR ends May 2025; Shiller still updates |
| Cash rate, pre-1926 | MeasuringWorth short-rate series | 1831+ documented (page fetched and quote verified 2026-10-31) |
| Independent annual cross-check, 1870+ | JST Macrohistory R.6 / RRoE replication data | 16–18 countries, annual total returns |
| Anything pre-1926 in monthly Damodaran form | Doesn't exist — don't try | Damodaran starts 1928 |

## Known gaps

- **Pre-1953 long rates in Shiller's file**: source undocumented on the
  data page; our own check (this session) found no methodology note.
- **What the AQR paper itself used for its bond benchmark**: not verified
  from the paper text this session; do not assume it matches Shiller's
  synthetic Treasury.
- **No free *traded* long-bond total-return index pre-1970** surfaced in
  the sources fetched for this page.
- **Shiller's dividend tail is provisional** (June 2026 vs. price's October
  2026 in the live file) — cap backtests a few months short of download
  month.
- **Date column gotcha**: dates are stored as decimal `YYYY.MM` numbers and
  Excel drops trailing zeros — October 2026 prints as `2026.1`. Parse with
  `year = int(x)`, `month = round((x − year) × 100)`; never by eyeball.
- MeasuringWorth cash-rate and macrohistory.net claims rested on
  search-result text at compile time; the review fetch of 2026-10-31
  verified both pages directly (quotes verbatim, confidence upgraded
  above). The macrohistory database's own end year, however, remains
  unstated by its download page (see annual cross-checks).

## See also

- [Commodities for the Long Run (AQR, 1877–2015)](commodities-for-the-long-run.md) — the commodity basket these legs pair with, and the state of its dataset
- [When Bonds Fail, What To Own Instead](when-bonds-fail.md) — what the bond leg's weaknesses look like in hot-inflation regimes
- [The Growth × Inflation Four-Quadrant Framework](growth-inflation-quadrants.md) — the state flags this backtest would condition on
