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

