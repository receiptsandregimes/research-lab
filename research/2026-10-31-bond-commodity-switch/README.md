# Bond ↔ Commodity switch (AQR basket)

## Question

Does switching between long-duration U.S. Treasuries and AQR's
long-run equal-weighted commodity basket — holding whichever has
recently outperformed on their relative-price trend — beat simply
holding a fixed blend of the two, over February 1877 – May 2025, when
tested in the 1877–1945 and 1946–2025 eras separately?

## Why it matters (owner's why)

*Drafted in Frank's voice from the 2026-10-31 conversation —
awaiting sign-off.*

> I want a defensive portfolio that passively protects itself across
> the long run: bonds while the world disinflates, commodities when
> inflation takes over. The relative price of bonds against a
> commodity basket is something I can compute myself, goes back
> further than any gold-based signal (gold is only usable post-1971),
> and is built on the see-saw my wiki documents: the AQR basket earns
> 14.8% in high-inflation states and −4.7% in low-inflation states,
> while bonds do the opposite. If a simple ratio switch beats holding
> both, I have a rule I can actually run; if it doesn't, I want to
> know that before I ever trust the idea with money.

## Status

Open — phase B: seeded with hypothesis, data pointers, and design
decisions; no numbers computed; memo awaiting Frank's round 1.

## Files

- `README.md` — this file: question, why, status.
- `2026-10-31-memo.md` — hypothesis split into falsifiable legs, prior
  art, design worries, test sketch, next actions.
- `SOURCES.md` — tiered reading list + data portals + do-not-cite list.

## Related wiki pages (inputs, not findings)

- [Commodities for the Long Run](../../llm-wiki/regimes/commodities-for-the-long-run.md) — the basket, its dataset (ends May 2025), and its state table.
- [Long-Horizon Stock & Bond Datasets](../../llm-wiki/regimes/long-horizon-stock-bond-datasets.md) — the verified bond leg (Shiller, 1871+).
- [The Four-Quadrant Framework](../../llm-wiki/regimes/growth-inflation-quadrants.md) — Gave's Currency Debasement Ratio, the gold-based ancestor of this signal.
