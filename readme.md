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

Dataset: 57 observations | 13 queries | 5 engines | Collected: March 2026

---

### 📌 General Patterns

* **List-based answers dominate** — nearly all engines return ranked lists or list/table hybrids regardless of query type
* **Review content is the most-cited content type** — "Best of" style roundups are the primary source layer AI engines pull from
* **Product pages are rarely surfaced directly** — retail pages appear occasionally but almost never as the top citation
* **Problem-solving queries don't cite brands** — queries like "how tight should climbing shoes be" or "how to choose ski boot size" return generic answers with no brand mentions across any engine

---

### 🏔️ SCARPA-Specific Findings

* **Overall citation rate: ~60%** — SCARPA appears in roughly 6 out of 10 engine-query pairs tested
* **Ski touring is the strongest category** — "best ski touring boots 2026" returned SCARPA at positions #1, #3, and #4 in Google AI Mode — the strongest single-query result in the dataset
* **Bouldering queries perform well** — SCARPA holds the #1 position in both Claude and ChatGPT for "top climbing shoes for bouldering"
* **Beginner queries are a significant gap** — "best climbing shoes for beginners" returned zero SCARPA mentions across Google AI Overviews, ChatGPT, and Claude
* **Trail running is a blind spot** — SCARPA was not cited in any trail running query; La Sportiva appeared consistently at positions #2–4
* **Brand framing gap vs. La Sportiva** — engines consistently describe La Sportiva as "the gold standard" or "the industry titan." SCARPA is labeled "precision engineers" — positive, but softer in authority signaling

---

### 🌐 Source & Domain Patterns

* **Reddit is the #1 cited domain** — appearing 18 times across all observations; community discussion is a primary trust signal for AI engines
* **Switchback Travel (12) and REI (10) are the next most cited** — review aggregators and large retailers dominate the citation layer
* **SCARPA's AI SERP visibility is downstream of third-party review presence** — engines are not pulling from brand.com; they are pulling from the sites that review and rank products

---

### ⚖️ Engine Behavior Notes

* **Claude and Gemini show higher SCARPA affinity** than ChatGPT for branded and comparison queries
* **Google AI Mode tends to return more product-specific results** than AI Overviews, which skews toward editorial content
* **ChatGPT cited zero SCARPA products** for the broad "best climbing shoes" query, favoring Evolv and La Sportiva

---

> These are working observations — not final conclusions. The dataset is early-stage and patterns will be validated as more queries and runs are added.



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
