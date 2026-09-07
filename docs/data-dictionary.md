# Data Dictionary

The dataset lives in [`../data/observations.csv`](../data/observations.csv). Each row is one query run against one engine. Columns are described below in order.

| # | Column | Description |
|---|--------|-------------|
| 1 | `Query` | The exact question asked. |
| 2 | `Intent_Type` | The kind of query. One of: `Informational`, `Comparison`, `Transactional`, `Problem-Solving`, `Consideration`. (Some brand-probe rows are left blank.) |
| 3 | `Engine` | Where it was asked: `Google/AI Overview`, `Google/AI Mode`, `ChatGPT`, `Gemini`, `Claude`. |
| 4 | `Cited_Domains` | Comma-separated list of every source the answer cited or referenced. Values like `None`, `No citations`, `Nothing cited`, or `AI Overview not generated` are recorded verbatim when applicable. |
| 5 | `Top_Domain` | If one source had to be named as the primary/most-prominent one, which was it. |
| 6 | `Content_Type` | The nature of the top source. Common values: `Review`, `Review/"Best of"`, `Retail`, `Forum`, `Guide`, `Editorial`, `Informational`, `Brand`. |
| 7 | `Answer_Format` | How the engine structured the answer: `List`, `Table`, `List/Table`, `Paragraph`, `Mixed`, `Discussion`, etc. |
| 8 | `Position` | Where the tracked brand (SCARPA) appeared in the answer. `0` or blank = not mentioned. A single number = its rank. Multiple numbers (e.g. `1,3,4`) = multiple SCARPA products appeared at those ranks. |
| 9 | `Notes` | Free-text analyst observations — the most interesting column. Captures oddities, exact quotes from the engine, competitor behavior, and anything noteworthy. |
| 10 | `Personalization_Level` | The session state during collection (e.g. `Incognito Mode`, `Logged in but temporary chat`, `Incognito, not logged in`). Blank on early rows. |
| 11 | `Date` | Collection date, ISO format (`YYYY-MM-DD`). |

## Controlled vocabularies

**Intent types** — `Informational` (discovery / general knowledge), `Comparison` (evaluating options), `Transactional` (purchase intent), `Problem-Solving` (fit, sizing, troubleshooting), and the occasional `Consideration` (worth-it / value questions).

**Content types** — sources are categorized as `Brand`, `Guide`, `Review`, `Retail`, `Editorial`, or `Forum`. In practice a `Review/"Best of"` variant was used heavily to distinguish ranked "best-of" listicles from straight reviews. Minor spelling variants exist in the raw notes (e.g. `Revew`); treat them as the intended label.

## A worked example

| Column | Value |
|---|---|
| Query | best climbing shoes for beginners |
| Intent_Type | Informational |
| Engine | ChatGPT |
| Cited_Domains | Treeline Review, Nomads with a Purpose, Switchback Travel, 99Boulders |
| Top_Domain | Treeline Review |
| Content_Type | Review |
| Answer_Format | List |
| Position | 0 |
| Notes | SCARPA isn't mentioned at all. |
| Personalization_Level | Logged in but temporary chat |
| Date | 2026-03-25 |

Reading it: for a beginner informational query, ChatGPT built its answer from review/aggregator sites, led with Treeline Review, and did not mention SCARPA at all.

## Notes on data hygiene

- Dates were normalized to ISO `YYYY-MM-DD` from the mixed formats used during collection (`25-Mar`, `4/8`, etc.).
- Empty separator columns and floating margin annotations from the original spreadsheet were dropped; the analyst's margin notes are preserved in [`../analysis/findings.md`](../analysis/findings.md).
- Text is otherwise left as originally recorded, including informal phrasing, so the raw observations stay faithful.
