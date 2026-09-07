# AI SERP Observation

A small, hand-collected study of **which sources AI search engines choose to cite** when answering outdoor-gear questions — and where the SCARPA brand does (and doesn't) show up in those answers.

> **Snapshot notice.** All observations in this repository were collected by hand between **March 25 and April 22, 2026**. AI answer engines change quickly, so the *findings* are a point-in-time snapshot, not a live measurement. The *methodology and schema*, however, are reusable — the study can be re-run at any time against current engines to build a trend line. See [`docs/methodology.md`](docs/methodology.md).

## What this project asks

Traditional SEO asks *"How do I rank #1?"* As AI-generated answers replace the classic list of blue links, the more useful question becomes:

**"When an AI answers a question, whose content does it choose to trust — and how do we get included in the answer?"**

Rather than tracking rankings, this study observes the *answers themselves*: the brands they mention, the domains they cite, the format they use, and where a specific brand (SCARPA) appears.

## The dataset at a glance

| | |
|---|---|
| **Observations** | 187 |
| **Unique queries** | 34 |
| **Engines tracked** | 5 — Google AI Overview, Google AI Mode, ChatGPT, Gemini, Claude |
| **Collection window** | 2026-03-25 → 2026-04-22 |
| **Category** | Climbing shoes, ski / touring boots, trail-running shoes |
| **Brand focus** | SCARPA (with La Sportiva as the recurring benchmark competitor) |

Each row is one query run against one engine. The full schema is documented in [`docs/data-dictionary.md`](docs/data-dictionary.md); the data lives in [`data/observations.csv`](data/observations.csv).

## Headline patterns

These are qualitative reads from the snapshot, not statistical claims. Fuller notes are in [`analysis/findings.md`](analysis/findings.md).

- **Third-party review and "best-of" content dominates.** The most-cited sources by a wide margin are aggregator/review sites — **Switchback Travel (41), Reddit (34), REI (21), Climbing Magazine (14), Outdoor Gear Lab (12)** — not brand-owned pages. "Review" and "Review/Best-of" together account for the majority of cited content types.
- **Brand pages are cited mostly for informational, not commercial, intent.** A brand's own site tends to surface when the query is generic/definitional ("SCARPA shoes"), and much less when the query is a shopping or comparison question.
- **La Sportiva is repeatedly framed as "the gold standard."** Across multiple engines, the competitor is described in definitive, authoritative language ("the industry titan," "the safest bet") — engines aren't just surfacing content, they're making brand claims to the consumer.
- **Small and niche sources punch above their weight.** Cited domains include a ~30k-follower Instagram account, sub-500-subscriber YouTube channels, and personal WordPress blogs — evidence that authority in AI answers isn't purely about size.
- **A fraudulent look-alike site was cited as a top source.** In one run, ChatGPT surfaced a fake "scarpa-boots.com" as its top-cited domain — a concrete brand-safety flag worth monitoring.

## Repository structure

```
ai-serp-observation/
├── README.md                  → this file
├── LICENSE                    → MIT
├── data/
│   └── observations.csv       → the 187-row dataset
├── docs/
│   ├── methodology.md         → how the data was collected + the query set
│   └── data-dictionary.md     → definition of every column and its allowed values
└── analysis/
    └── findings.md            → qualitative insights and patterns from the snapshot
```

## Reusing this

Clone or download, open `data/observations.csv` in any spreadsheet tool, and filter by `Engine`, `Query`, or `Content_Type`. To extend the study, follow [`docs/methodology.md`](docs/methodology.md) and append new rows using the same schema, dating each batch so historical and fresh observations stay comparable.

## Author & scope

Collected and maintained by Chase Barrett (eCommerce Specialist, SCARPA North America) as an independent observation exercise. Proprietary product copy, performance data, and internal figures are intentionally excluded; this repository contains only publicly observable AI-answer behavior and the analyst's own notes.
