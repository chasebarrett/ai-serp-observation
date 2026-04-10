# AI SERP Observation 👋  
**AI Search | SEO Evolution | Data Observation**

I’m interested in how AI systems are changing the way information is discovered, not just how content is ranked, but how it’s selected, summarized, and presented.

This repository documents an ongoing project focused on understanding how AI-driven search engines (ChatGPT, Google AI Overviews, Claude, etc) choose which sources to include in their answers.

Rather than relying on assumptions, this project is built around direct observation — tracking queries, responses, and patterns over time.

---

## 🧭 The Problem

Search is shifting from:

- Lists of ranked links  
- To **generated answers built from multiple sources**

### ⚠️ Core Issue

Traditional SEO answers:
> “How do I rank?”

AI search introduces a different question:
> **“How do I get included?”**

---

### 📉 Why This Matters

- A page can rank well and still not appear in AI answers  
- AI systems may prioritize different signals than traditional search  
- Visibility is becoming **less about position and more about selection**

This creates a gap in understanding:
> What actually drives inclusion in AI-generated results?

---

## 🧪 The Experiment

This project is built on a simple idea:

> Ask AI systems questions — and track which sources they choose to trust.

---

### 🔍 Process

For each query:

1. Run the query in an AI search engine  
2. Review the generated answer  
3. Capture:
   - Which domains are mentioned  
   - Which source appears most prominent  
   - The type of content represented  
   - The structure of the answer  
4. Log observations into a structured dataset  

---

## 🏗️ Dataset Structure

Each observation is recorded as a single row.

### 📊 Fields

- `Query`
- `Intent_Type`
- `Engine`
- `Cited_Domains`
- `Top_Domain`
- `Content_Type`
- `Answer_Format`
- `Position`
- `Notes`

---

### 📈 Example

| Query | Intent_Type | Engine | Cited_Domains | Top_Domain | Content_Type | Answer_Format | Position | Notes |
|------|------------|--------|---------------|------------|--------------|--------------|----------|------|
| best climbing shoes for beginners | Informational | ChatGPT | REI, La Sportiva, Scarpa | REI | Guide | List | 3 | Aggregators dominate, brands secondary |

---

## 🧠 My Approach

Rather than trying to reverse-engineer AI systems directly, this project focuses on:

- Consistent observation  
- Clean data capture  
- Pattern recognition over time  

The goal is not to prove how AI works internally, but to understand:
> **what it consistently chooses to show**

---

## 🔑 Early Observations

Dataset: 127 observations | 22 queries | 5 engines | Collected: March – April 2026

---

### 📌 General Patterns

* **List-based answers dominate** — nearly all engines return ranked lists or list/table hybrids regardless of query type
* **Review content is the #1 cited content type** — editorial roundups and "best of" pages account for 52% of all cited sources across every engine and query
* **Problem-solving queries don't cite brands** — queries like "how tight should climbing shoes be" or "how to choose ski boot size" return generic answers with no brand mentions, confirmed across 25 runs with a 4% citation rate
* **Intent type is the strongest predictor of brand inclusion** — stronger than engine choice; Comparison queries return SCARPA 93% of the time, Problem-Solving only 4%
* **AI engines are not replicating Google's authority hierarchy** — 56% of all citations go to small or mid-sized domains that would not rank highly by traditional SEO metrics

---

### 🏔️ SCARPA-Specific Findings

* **Overall citation rate: ~53%** — SCARPA appears in roughly 53 out of 100 engine-query pairs tested; down from an early 60% as the sample grew and more problem-solving and ski boot queries were added
* **Branded queries are 100% cited** — "scarpa instinct vs drago," "best SCARPA climbing shoes," and "scarpa vs la sportiva mountaineering boots" all return SCARPA at position #1 across every engine tested
* **Ski touring is the strongest non-branded category** — "best ski touring boots 2026" returned SCARPA at positions #1–4 across 7 runs; the Maestrale RS is the most frequently surfaced product by name
* **SCARPA is a consistent #2 in advanced climbing shoe queries** — but La Sportiva holds #1 across all 10 runs of "Top climbing shoe brands for advanced climbers," described as "the gold standard" or "the industry titan" by ChatGPT, Claude, and Gemini
* **Beginner queries remain underperforming** — "best climbing shoes for beginners" sits at 56% citation rate, but SCARPA appears at position #3–5 and is often labeled a "specialty choice"
* **Trail running is a complete blind spot** — zero SCARPA citations across all trail running queries; La Sportiva appears at positions #2–4 every time
* **Ski boots are the largest category gap** — zero citations across 22 ski boot query runs (beginner, wide-fit, sizing); Rossignol, K2, and Tecnica dominate; the content type being cited is Review — meaning the format is right but SCARPA has no presence in those roundups

---

### 🌐 Source & Domain Patterns

* **Switchback Travel is the single most cited domain** — 28 appearances across climbing shoes, bouldering, ski touring, and ski boots; it is the highest-leverage third-party platform for AI SERP visibility
* **Reddit (26) and REI (14) round out the top three** — these three domains alone account for nearly half of all citations
* **56% of all citations go to small or mid-sized domains** — 83 citations to small domains (57 unique) and 91 to mid-sized domains; AI engines are drawing from a far wider and flatter web than traditional SEO rankings would predict
* **Geographically niche and low-authority retailers are being cited** — SportShoes.com (UK), Varuste.net (Finland), basecamp-shop.com (Germany), Telemark Pyrénées (France), Bentgate Mountaineering (Colorado), AlpinStore (EU), and Oliunid (EU) all appear as cited sources despite modest traditional SEO footprints
* **Butora USA appears 8 times** — more than SCARPA's own website — largely by publishing educational content that directly answers problem-solving queries

---

### ⚙️ Engine Behavior Notes

* **Engines are converging** — citation rate spread across all five engines is only 9 points (Claude/Google AI Mode at 57%, ChatGPT at 48%)
* **Claude and Google AI Mode lead** in SCARPA citation rate; ChatGPT trails slightly
* **Google AI Overview and AI Mode pull more from Informational content** than other engines — which is why they surface fewer brands; Informational pages cite SCARPA only 11% of the time
* **ChatGPT and Claude lean on Review content** — which is where SCARPA has the most presence

---

### 🔍 Emerging Hypothesis: AI Citation ≠ SEO Rank

The presence of small, geographically niche, and low-authority domains in AI citations suggests AI engines are not simply reproducing Google's link-authority hierarchy. What these domains appear to share is **structured, specific, and complete product data** — detailed spec pages, size runs, product descriptions — that make them legible to AI models regardless of their traffic or backlink profile.

This points to an important strategic reframe:

> AI SERP visibility may be less about outranking established players and more about being **present, specific, and well-structured** wherever a product is discussed online.

For SCARPA, this suggests:
* Product data quality and completeness — on brand.com and with retail partners — may directly influence AI citation behavior
* The barrier to being cited by AI could be lower than traditional SEO would imply
* A deliberate data-seeding strategy with specialty retailers could expand AI footprint intentionally

---

> These are working observations — not final conclusions. The dataset is active and patterns will continue to be validated as more queries and runs are added.

---

## 🧩 Query Types

Queries are grouped into:

- **Informational** — discovery and general knowledge  
- **Comparison** — evaluating options  
- **Transactional** — purchase intent  
- **Problem-Solving** — fit, sizing, troubleshooting  

---

## 🧠 Content Types

Observed sources are categorized as:

- Brand  
- Guide  
- Review  
- Retail  
- Editorial  
- Forum  

These may evolve as the dataset grows.

---

## ⚖️ Bias & Personalization

AI outputs can vary based on:

- account history  
- session context  
- location  
- platform-specific behavior  

To reduce noise where possible:

- queries may be run in fresh sessions  
- prompts are kept consistent  
- results are compared across engines  

This project assumes variability — not uniform results.

---

## 📈 Why This Matters

This project explores a shift from:

> Ranking → Inclusion  

Understanding that shift has implications for:

- SEO strategy  
- Ecommerce visibility  
- Content structure  
- Brand presence in AI systems  

---

## 📁 Repository Structure

```text
ai-serp-observation/
├── README.md
├── data/
│   ├── raw/
│   └── processed/
├── methodology/
│   ├── query-framework.md
│   └── logging-guidelines.md
├── findings/
│   └── notes.md
├── dashboards/
└── assets/
```

---

## 🚧 Status

This is an ongoing project.

The dataset, methodology, and findings will continue to evolve as more queries are tested and patterns become clearer.

---

> **This repo is less about conclusions, and more about building a structured way to observe how AI systems make decisions.**
