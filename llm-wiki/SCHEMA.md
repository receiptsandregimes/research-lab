# Wiki Schema

Per-project conventions. LLM proposes changes; user approves. Co-evolves
with the wiki. This wiki is **public** — the Public-record rules below are
law, not guidance.

## Domain

Trading, investing, and portfolio research: market regimes, edge/strategy,
risk and position sizing, trade post-mortems ("receipts"), and trader
psychology. In scope: anything that can improve a decision Frank actually
makes with money. Out of scope: general finance news, product reviews, and
long-form books (articles, papers, transcripts, and chats only, for now).

## Public-record rules (override everything else)

- **Publish gate.** Nothing enters the public repo without Frank's explicit
  sign-off. The agent writes; Frank approves.
- **Never delete, correct.** Superseded claims are marked, not removed.
  Corrections use the `### Correction:` pattern and stay visible.
- **No copying paywalled or licensed material.** Reference by URL or
  path. Copy into `raw-sources/` only material we may redistribute.
- **Redact.** No account numbers, broker identities, real dollar positions,
  or names of other people. Positions and P&L appear as ranges or indexed
  percentages unless Frank explicitly opts in to exact figures.
- **No references to private tooling or private file paths** in any page
  in this repo.

## Source buckets

By kind of source. New buckets need user approval + a SCHEMA update.

- `articles/` — blog posts, web clippings, threads
- `papers/` — academic papers, preprints, research notes
- `transcripts/` — talks, podcasts, videos
- `conversations/` — chat dumps, agent sessions
- `notes/` — pasted text, ad-hoc

(No `books/` bucket yet — books are out of scope by domain choice.)

## Topic taxonomy

By subject, not by kind. New topics need user approval.

- `regimes/` — market regime research: definitions, detection, history,
  what works in each
- `edge/` — candidate edges and strategies: hypotheses, evidence, status
- `risk/` — position sizing, drawdown discipline, portfolio construction
- `receipts/` — post-mortems of Frank's own trades and calls (redacted)
- `psychology/` — the game: discipline, bias, accountability

## Confidence rubric

Applied to claims and open questions on compiled pages (`confidence:` in
frontmatter or inline markers). Log changes to confidence — downgrades
especially.

- **low** — one source, or a vibe Frank can't yet defend under pressure.
- **medium** — two or three independent sources agree; no numbers yet.
- **high** — primary evidence: price data, a backtest, a backable document.

A claim moves *down* the moment contrary primary evidence appears; that
event gets its own `log.md` entry.

## Page types

- `concept`, `decision`, `bug`, `open-question`, `source`, `reference`,
  `synthesis`, `stub` — see the wiki skill.
- Concept variants (taxonomy, implementation walkthrough) are shapes a
  `concept` may take, not new types.
- In this wiki, `open-question` pages are the handoff to `research/`: the
  question board in `research/questions.md` points at them.

## Lint rules

- Stale-claim threshold: 30 days.
- Relative path verification: every `](*.md)` link must resolve from the
  file's directory.
- Bidirectional links: if page A links to page B, page B links back.
- Redaction sweep (public-wiki specific): flag any dollar amount tied to a
  real account, broker name, or account number in compiled pages.
- Confidence presence: every `open-question` and every `edge/` claim page
  must carry a `confidence:` value.

## Notes

- Two-layer design: `research/` (process, dead ends, diary) feeds
  `llm-wiki/` (distilled knowledge). Conclusions get "filed upstairs"
  when an investigation closes; the flailing stays in `research/`.
- Glossary: to be built as terms stabilize.
