# Methodology

## The experiment in one sentence

We reverse-engineer AI search by observing which content each engine chooses to include in its answers — the brands it mentions, the domains it cites, and the format it uses — rather than by tracking rankings or clicks.

## The core question

For every query, we are trying to answer: *when an AI answers this question, whose content does it trust enough to include?* Old SEO optimized for a position on a results page. In an answer-engine world, the goal shifts from **ranking** to **inclusion** — being one of the sources the model summarizes.

## How each observation was collected

Each row in [`../data/observations.csv`](../data/observations.csv) is a single query run against a single engine, captured in four steps:

1. **Ask a question.** Pull a query from the fixed query set (below) and run it in one engine.
2. **Read the answer, not the links.** Focus on the narrative answer the engine produces, not the traditional list of results underneath it.
3. **Ask "where did this come from?"** Note the brands mentioned, the websites cited, and the *type* of source (review, retail, forum, brand, editorial, guide).
4. **Write it down.** Record one row using the schema in [`data-dictionary.md`](data-dictionary.md).

### Engines observed

- **Google — AI Overview**
- **Google — AI Mode**
- **ChatGPT**
- **Gemini**
- **Claude**

### Session conditions

Personalization can skew what an engine cites, so the session state was recorded per observation in the `Personalization_Level` column (e.g. *Incognito Mode*, *Logged in but temporary chat*, *Incognito, not logged in*). Later batches were standardized toward incognito / logged-out sessions to reduce personalization bias. Because conditions were not identical across the whole collection window, comparisons should weight the later, more consistent batches more heavily.

## The query set

Queries were chosen to span four intent types and to include both category-generic and SCARPA-specific phrasing. They are grouped by intent:

- **Informational** — discovery and general knowledge (e.g. *best climbing shoes for beginners*, *best ski touring boots 2026*, *top climbing shoes for bouldering*).
- **Comparison** — evaluating options (e.g. *scarpa vs la sportiva climbing shoes*, *scarpa instinct vs drago*, *scarpa quattro vs la sportiva synchro*).
- **Problem-Solving** — fit, sizing, and troubleshooting (e.g. *how tight should climbing shoes be*, *how to choose ski boots size*, *what flex rating do I need for intermediate skiing?*).
- **Transactional / Consideration** — purchase-leaning intent (e.g. *where to buy high-quality climbing shoes online*, *are expensive climbing shoes worth it*).

Brand-name probes (*SCARPA*, *SCARPA shoes*, *SCARPA boots*, *SCARPA climbing shoes*, *best SCARPA climbing shoes*, *scarpa climbing shoes review*) were added to test how engines handle direct brand queries.

The full list of 34 queries is preserved in the source dataset's `Queries` tab and is reflected in the `Query` column of the CSV.

## Guiding principle

**Volume over perfection.** The value comes from consistency across many observations, not from getting any single row exactly right. Intent labels and content-type labels were kept consistent so that patterns could surface once ~20–30 rows accumulated.

## Known limitations

- Hand-collected and subjective in places (`Top_Domain`, `Content_Type`, and `Position` involve analyst judgment).
- Session conditions vary across the collection window (see above).
- A point-in-time snapshot; engine behavior in these products changes frequently.
- Coverage is concentrated in climbing and ski footwear, reflecting the SCARPA brand focus.
