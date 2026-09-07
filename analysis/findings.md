# Findings

Qualitative reads from the March 25 – April 22, 2026 snapshot (187 observations, 5 engines, 34 queries). These are pattern observations, not statistical claims — the sample is hand-collected and the collection conditions varied over the window. Where a count is given, it is a raw tally from [`../data/observations.csv`](../data/observations.csv).

## 1. Review and "best-of" content is what gets cited

By a wide margin, the sources AI answers pull from are third-party review and aggregator sites, not brand-owned pages. Most-cited domains across the snapshot:

| Domain | Times cited |
|---|---|
| Switchback Travel | 41 |
| Reddit | 34 |
| REI | 21 |
| Climbing Magazine | 14 |
| SCARPA North America | 13 |
| Outdoor Gear Lab | 12 |
| GearJunkie / GearLab | ~20 combined |
| Treeline Review | 8 |
| The Ski Monster | 8 |
| Butora USA | 8 |

By content type, `Review` and `Review/"Best of"` together account for the majority of top-cited sources, well ahead of `Retail`, `Forum`, `Guide`, and `Editorial`. **The engines love ranked "best-of" listicles.**

## 2. Brand sites surface for information, not for shopping

A brand's own website is cited *seldom*, and when it is, it's almost always for **informational** content rather than commercial intent. SCARPA North America appears most often on generic/definitional brand queries ("SCARPA shoes," "SCARPA climbing shoes") and much less on comparison or "best" queries. A recurring note in the data: engines reward content phrased as neutral expertise ("how to size ski boots") over content phrased as brand-owned ("how to size *our* ski boots") — *less expert on "us," more expert on "this."*

## 3. Competitor framing is a real exposure

Across multiple engines, **La Sportiva is repeatedly cast as "the gold standard,"** "the industry titan," and "the safest bet." The engines don't merely surface competitor content — they make definitive brand claims to the consumer. Representative notes from the dataset:

- Claude, on *best climbing shoe brand*: *"If you can only pick one, La Sportiva is the safest bet for quality and variety."*
- Gemini, on advanced climbers: calls La Sportiva "The Industry Titan" and SCARPA "The Precision Engineers," and specifically credits designer Heinz Mariacher to SCARPA's success.
- One output describes SCARPA as "Narrow," directly contradicting other outputs that call it "wide" — inconsistency the brand can't currently control.

This is the strategic core of the study: **when the answer *is* the interface, an unmanaged competitor narrative becomes the default answer.**

## 4. Small and niche sources punch above their weight

Authority in AI answers is not purely about domain size. Cited sources in the snapshot include a ~30k-follower Instagram account (as the *top* source on a mountaineering-boots query), YouTube channels with 300–400 subscribers, and personal WordPress blogs. As one engine put it when asked about this pattern, it's "kind of leveling the playing field… you could benefit not only from major reviews but also from micro-communities." Practically: earned mentions in engaged niche communities may matter more than raw reach.

## 5. Brand-safety flag: a fraudulent look-alike was cited

On the query *SCARPA boots*, **ChatGPT surfaced a fake "scarpa-boots.com" as its top-cited domain.** An answer engine presenting a fraudulent storefront as an authoritative brand source is a concrete, monitorable risk — worth flagging to brand-protection and worth re-checking on any future data pull.

## 6. Structural observations for reframing SEO

- **Inclusion, not ranking.** In a zero-click answer, "you show up or you don't — there is no follow-up." The optimization target moves from position to *presence in the summary*.
- **Granularity is lost.** Engines will state a use case, but nuance and product-level differentiation get flattened in summarization.
- **"Best-of" structure is the currency.** Content that is structured, comparative, and citation-ready is what gets pulled in.

## What this points toward (not yet tested here)

The snapshot suggests, but does not prove, a content strategy centered on: earning placement in the review/aggregator sites the engines already trust; publishing brand-owned content in neutral, expert, citation-ready formats rather than promotional ones; monitoring competitor framing and fraudulent-source citations as ongoing risks; and cultivating niche-community mentions. Confirming any of this would require re-running the study over time — which the [methodology](../docs/methodology.md) and schema are built to support.
