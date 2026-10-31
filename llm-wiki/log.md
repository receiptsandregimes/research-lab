# Log

Append-only operation log for the wiki. Semantic entries: what knowledge
changed and why, not file diffs.

## [2026-10-30] setup | wiki scaffolded
- Created schema (topics: regimes, edge, risk, receipts, psychology),
  confidence rubric (low/medium/high), and public-record rules
  (publish gate; never delete, only correct; no paywalled copies;
  redaction of account details).
- Two-layer design agreed: `research/` diary feeds distilled
  conclusions into this wiki.
- No sources ingested yet.

## [2026-10-30] register | Growth × inflation four-quadrants framework (5 sources)
- Registered five web sources on the two-axis (growth, inflation) regime
  framework and per-quadrant asset performance: Bridgewater All Weather
  Story (primary source; axes = surprises vs. priced-in expectations),
  Portfolio Optimizer on Charles Gave's Four Quadrants (1978 origin claim;
  stock/oil and bond/gold ratios as quadrant detectors), Man Group
  regime-based investing (empirical/skeptical treatment), ReSolve
  structural diversification (pricing mechanics per regime), Swoopr
  overview (plain modern map; weakest source).
- Open question for compile: level-vs-surprise definition of the axes.
- All registered by URL (stable, public); nothing copied. Compile pending.

## [2026-10-30] compile | Growth × inflation four-quadrants framework (5 sources → 2 pages)
- First compile. Created `regimes/growth-inflation-quadrants.md`
  (concept: two axes, four regimes, naming map across Gavekal/Man/
  Bridgewater vocabularies; origin history Gave 1978 → Browne 1982 →
  Dalio 1996; detection via Gave's energy-efficiency and
  currency-debasement ratios vs indicator lists) and
  `regimes/asset-performance-by-quadrant.md` (reference: per-quadrant
  favored/avoided assets with structural mechanics per ReSolve, plus
  Man Group's empirical fine print — their "always worked" findings,
  the stagflation-breaks-60/40 consensus, and the value-spray myth).
- Central definitional conflict flagged as open question and annotated
  in the concept page: level/direction (Gave, ReSolve, Swoopr) vs
  expectation-surprise (Bridgewater) axis definitions. Unresolved;
  must be settled before any live detector is built.
- Known-gaps section names what the sources DON'T give us (no
  precision numbers for backtesting a tilt; Gavekal primary docs
  secondhand only).
- Updated: index.md (regimes section now live; first pages in wiki).

## [2026-10-30] correction | QA pass, same-day — 4 accuracy errors fixed
- Verified the compile's claims against the fetched texts of all five
  registered sources. Most check out exactly (ratios, dates, quotes
  "obese pitches"/"ALWAYS worked", TIPS 10%, 32% Treasuries+T-bills,
  Swoopr indicator lists, 5–15pp tilts, seven-regime/six-strategy Man
  test, FIRE/ICE four-state split). Fixed what didn't:
- asset-performance: "T-bills hedge both inflation surprises and
  slowing growth" was wrongly credited to Bridgewater's framing (the
  All Weather PDF never mentions T-bills) — it is ReSolve's claim;
  re-attributed with inline correction note.
- asset-performance: claimed the Gavekal asset map was "relayed
  secondhand" via portfoliooptimizer.io and an unregistered "Brian
  Pate overview" — neither checks out; portfoliooptimizer.io has no
  asset map (only quadrant definitions + detector ratios). The
  stagflation consensus is recut from "all four" sources to the three
  verifiable ones (Bridgewater, ReSolve, Swoopr); formal
  `### Correction:` block added.
- asset-performance: misquote fixed — ReSolve's title is
  "…All Seasons," not "…Seasones."
- growth-inflation-quadrants: unsourced era examples (stagflation
  "1973–75, 2022"; deflation "2008 crisis") removed in favor of eras
  the sources actually name (Great Depression, 1981–2000,
  2003–mid 2008 via ReSolve); Gavekal Goldilocks name corrected from
  ReSolve's "disinflationary boom" to Gave's "Deflationary boom" per
  the registered relaying source; `### Correction:` block added.
- Bookkeeping: the levels-vs-surprises open question is now on the
  research question board (research/questions.md), per schema.
- Citation precision note (no change made): Man Group article cited as
  "The Road Ahead, May 2026" matches the edition date shown on the
  page, but the page's embedded metadata says first published
  2024-02-15. Left as-is for now.


## [2026-10-30] archive | When Bonds Fail, What To Own Instead
- Filed query answer as synthesis page regimes/when-bonds-fail.md,
  connecting the quadrant framework and the per-quadrant performance
  reference: bonds lose when inflation rises (reflation, stagflation);
  per-regime alternatives; Man Group's evidence bonds shield only about
  half of equity bear markets. Cascade: See-also links added to both
  cited pages.

## [2026-10-31] register | Commodities for the Long Run (5 sources)
- Registered AQR's long-run commodities paper in both versions plus its
  public dataset pages: NBER Working Paper 22793 (November 2016, Levine/
  Ooi/Richardson — full 40-page PDF fetched), the published FAJ article
  (registered by DOI; the publisher page returned "access denied", so the
  journal full text was NOT fetched), the CFA Institute Research and
  Policy Center landing page (relays the published abstract; JSON-LD
  datePublished 2018-04-02), AQR's own journal-article page (abstract,
  April 30 2018, four authors incl. Caroline Sasseville), and AQR's two
  dataset pages (monthly-updated index level data; original paper data
  through December 2015).
- Dataset spreadsheets referenced by URL only, not copied into
  raw-sources/ — AQR/author copyright, fails the schema's redistribution
  test.
- Date metadata discrepancy captured at register time: the same article is
  dated 2 April 2018 (CFA page), April 30, 2018 (AQR page), and vol 74(2),
  pages 55-68 (NBER's citation of it). Left unreconciled; cite the edition
  actually read.

## [2026-10-31] ingest | Commodities for the Long Run (AQR, 1877–2015)
- Compiled regimes/commodities-for-the-long-run.md. Verified claims against
  the fetched working-paper text (each quoted phrase and number grepped in
  the PDF extraction) and the fetched relay pages for the published
  abstract.
- New knowledge: the commodity premium splits by driver. Backwardation
  pays through carry (adjusted carry 12.2% vs −3.6%, while excess spot is
  *lower* in backwardation, −2.9% vs 6.5%); inflation pays through spot
  (10.4% vs −5.8%, with essentially the same index volatility in both
  states). Also the paper's own limits: not equity-like returns, carry —
  much of it the short rate — the bigger historical contributor, only 8%
  R-squared for the monthly state regression, and the equal-weighted
  index's investability objection.
- Primary verification (ours, not the sources'), stated as confidence:
  high on the page: AQR's monthly dataset has stopped updating. Live file
  ends 2025-05-30 with Last-Modified 2025-06-21 (same header on a
  cache-busting request); 1,780 monthly rows 1877-02-28 → 2025-05-30 with
  no gaps or duplicate months; Internet Archive copies of the page from
  2025-09-14, 2026-02-09 and 2026-05-11 all still display "May 30, 2025";
  control test on AQR's Momentum Indices Monthly shows Last-Modified
  2026-10-05 with September 2026 data, so AQR is updating other datasets
  and this one has been quiet ~17 months. Consequence for any future work:
  May 2025 is the hard end of the public sample, and the file is
  index-level only (11 columns), so the portfolios cannot be rebuilt from it.
- Unverifiable and excluded: the 2018 journal full text (publisher 403).
  Two published-version sentences about returns conditional on curve shape
  appeared in search snippets but do not grep in any fetched copy — left
  off the page rather than cited secondhand.
- Extraction caveat recorded on the page: the PDF-to-text dump splits some
  words ("commodit y", "14. 8%"), so quote checks need a space-tolerant
  grep.
- Cascade: See-also links added to growth-inflation-quadrants.md,
  asset-performance-by-quadrant.md and when-bonds-fail.md. The
  asset-performance "no source gives returns precise enough to backtest a
  tilt" gap is now **marked** partially superseded (kept, not deleted, per
  the never-delete rule) — AQR does give single-state numbers, still not a
  two-axis quadrant cross.
- Confidence: medium on the paper's evidence (single research team; the
  paper discloses that AQR "offers financial products that invest in
  commodities"); high on the dataset-status section (primary check).
- Updated: index.md (fourth page in regimes/).
- Self-check (mechanical, same session): every quoted span (39) and every
  numeric token in the paper sections (100) was matched against the
  fetched source text with whitespace-insensitive matching. All matched
  except the two documented extraction artifacts and the AQR-page/dataset
  figures, which match the fetched AQR pages or our own file inspection.
  Two fixes made in place before any commit, so no `### Correction:`
  block was needed: (a) the −0.27 low-inflation figure was first written
  as a return on when-bonds-fail.md — it is a Sharpe ratio in the paper's
  Sharpe passage; (b) the em-dash section heading was retitled so its
  anchor is unambiguous under both anchor-slug conventions.
- Lint: 0 issues across the 4 compiled pages (frontmatter, links, anchors,
  index sync, See-also bidirectionality, Contents block, redaction sweep).

## [2026-10-31] register | Long-horizon stock & bond datasets (11 sources)
- Registered under papers/ (dataset-page precedent set by the AQR rows):
  shiller-online-data, shiller-ie-data-yale-mirror, fred-gs10-table,
  fred-gs10-series, damodaran-histret-1928, measuringworth-datasets,
  measuringworth-interest-sources, jordà-etal-2019-rroe-nber,
  rroe-replication-dataverse, jst-macrohistory-db.
- Fetch status: shillerdata.com page + live ie_data.xls, Yale-mirror
  ie_data.xls, NBER w24112 page, Damodaran histret.html, MeasuringWorth
  /datasets/ — all fetched directly 2026-10-31. FRED (both pages),
  macrohistory.net, Harvard Dataverse (DOI), and MeasuringWorth
  interest-rates sources2.php — not fetchable from this machine (DNS/
  refused); claims from those four rest on same-day search-result text
  and are marked medium confidence on the page.

## [2026-10-31] ingest | Long-Horizon Stock & Bond Datasets for the 60/40 Legs
- Compiled regimes/long-horizon-stock-bond-datasets.md (reference,
  confidence: high) as the pairing answer for backtests on the AQR
  equal-weight basket: Shiller's monthly file (Jan 1871–Oct 2026, 1,870
  gapless rows) as stock + bond legs; Jordà/Schularick/Taylor annual
  datasets as cross-checks; Damodaran rejected (1928+, annual).
- Verified by primary file inspection, not prose: coverage and gaps
  counted from the date column; the bond column re-derived from the
  file's own rate column (par 10-yr Treasury, coupon = month-t yield,
  1-month hold, marked at month t+1 with 119 periods left) with max
  difference 1.6e-15 over all 1,869 populated months; Sept-2026 rate
  4.99 cross-matched against FRED's GS10 page; Yale mirror file shown
  stale (properties saved 2023-09-17, data ends 2023.09).
- Correction of record: an interim claim in the working conversation
  said the official 10-year series starts 1962; FRED's GS10 table page
  says "Date Range 1953-04-01 to 2026-09-01". The page carries 1953.
- Not verified (said so on the page): what the AQR paper itself used
  for its bond benchmark; the construction of Shiller's pre-1953 rate
  stand-in; paid databases (none cited in our sources).
- Self-check (same session): all quoted spans re-grepped against the
  fetched/searched texts; two fixes made in place pre-commit — (a) the
  FRED series title had been truncated inside quotation marks, restored
  verbatim; (b) the "Sep 2026: 4.99" claim was cited to the FRED table
  page but appears on the series page — series page registered and the
  citation retargeted. Link/anchor/slug/bidirectionality lint: 0 issues.
- Updated: regimes/commodities-for-the-long-run.md (See also),
  regimes/when-bonds-fail.md (See also),
  regimes/growth-inflation-quadrants.md (See also), index.md.

## [2026-10-31] fix | accuracy review of the datasets ingest — 2 P2s + 1 P3 fixed, 2 confidence upgrades
- Independent review of the same-day datasets ingest, per the review
  procedure: every registered source re-fetched fresh (10 dataset rows
  plus the AQR page) and the NBER w22793 paper PDF re-fetched; the live
  and mirror Shiller files re-downloaded and every number re-derived
  from scratch. Verdict: the page is accurate. Of ~35 registered
  checkable claims, all verified clean except the three fixed below.
- Independently reproduced from the files: 1,870 gapless monthly rows
  1871.01→2026.10 (no dups); the synthetic-bond formula match over all
  1,869 populated months (review max diff 1.8e-15 — same "exact to
  rounding" verdict, the sub-digit gap vs the compile's 1.6e-15 is
  float arithmetic order); all return/vol/extreme stats (9.64/14.13 and
  10.95/12.10 stocks; 4.85/4.29 and 5.75/6.14 bonds; extremes −8.26 and
  +10.90); the 2026.1 date-column quirk; every verbatim quote on the
  page (Shiller page construction notes, Damodaran title and date,
  MeasuringWorth titles, NBER title/authors/QJE 134(3) 2019 pp.
  1225–1298 and abstract, macrohistory R.6, AQR "May 30, 2025" dataset
  date, "60/40" and "54/36/10" portfolio exercises and 6.7% stock excess
  return from the paper text).
- FRED note: fred.stlouisfed.org still does not resolve from this
  machine; FRED claims verified via same-session search-result page
  text — series title, "Sep 2026: 4.99", "Date Range 1953-04-01 to
  2026-09-01", all exact.
- P2 fixed — Yale mirror pointer drift: the stale-monthly-file facts
  (saved 2023-09-17, 1,833 rows, data ends 2023.09) were true —
  re-verified against the file itself at econ.yale.edu/~shiller/
  ie_data.xls — but were credited to the data.htm page, which no
  longer links that file (its only download today is an annual
  1871–2016 file). The direct file URL is now registered
  (shiller-ie-data-yale-file, added to the page's sources), and the
  bullet carries an inline correction.
- P2 fixed — "their papers' windows end in 2015" was verified only for
  the RRoE paper; the macrohistory download page nowhere states an end
  year. Claim scoped to what the sources say, with inline correction.
- P3 fixed — the Dataverse DOI was registered uppercased
  (10.7910/DVN/GGDQJ) and returns "Error: DOI Not Found" (DOI
  resolution proved case-sensitive in practice this session); the
  registry now pins the lowercase resolving form (10.7910/dvn/ggdqgj).
  The page's Dataverse claim (dataset title, published 2019-03-26) was
  verified exact via fresh search-result record.
- Confidence upgrades — macrohistory.net and the MeasuringWorth
  interest-rates page were unfetchable at compile time (claims rested
  on search-result text, marked medium); both fetched directly during
  the review and their quotes matched verbatim → upgraded to high,
  upgrade marked inline on the page (and the "pending fetch" table row
  and Known-gaps bullet updated to match). The synthetic-bond max-diff
  figure on the page was left as-is (same magnitude, both "exact to
  rounding").
- Tuning loop: two new failure patterns — URL case-mangling at
  register time, and file evidence cited to a page that no longer links
  it — codified as new rules in the ingest procedure.
- Bookkeeping lint: otherwise clean — index sync, bidirectional
  See-also both directions, all cited slugs registered, no anchor
  links used, redaction sweep clean, frontmatter valid, question board
  untouched (no open questions created or resolved). The uncommitted
  ingest was committed as-reviewed first (a4bfd76), then these fixes as
  a separate fix: commit.
