# research-assistant-cli

## Research Publications

Ten papers across ML, NLP, computer vision, cybersecurity, and systems. Full index with PDFs, LaTeX source, and Overleaf-ready templates in [papers/](papers/).

| # | Paper | PDF |
|---|-------|-----|
| 1 | WarLens: Transfer Learning for Event Classification in Conflict Zones | [PDF](https://github.com/omprxkash/warlens/blob/main/docs/paper/WarLens%20%E2%80%93%20Transfer%20Learning%20for%20Event%20Classification%20in%20Conflict%20Zones.pdf) |
| 2 | LLM-Augmented OCR for Robust Document Understanding + Patent | [PDF](https://github.com/omprxkash/llm-aided-ocr/blob/main/docs/research/21BCE1950_53074.pdf) |
| 3 | GemVAE: Graph-Enhanced Multi-Modal VAE for Image Classification | [PDF](https://github.com/omprxkash/graph-attention-vision-transformers/blob/master/paper/GemVAE_Pugazhendhi_2023.pdf) |
| 4 | Intrusion Detection Using ML and Neural Network Approaches | [PDF](https://github.com/omprxkash/intrusion-detection-system-cyber/blob/main/INTRUSION_DETECTION_IN_A_NETWORK_USING_MACHINE_LEARNING_AND_NEURAL_NETWORK%5B1%5D.pdf) |
| 5 | Multi-Disease Prediction Using Ensemble Machine Learning | [PDF](https://github.com/omprxkash/disease-prediction-ml/blob/main/21BCE1950_21BCE5828_DA3_afterreview.pdf) |
| 6 | BERT-Based Named Entity Recognition for Domain-Specific IE | [PDF](https://github.com/omprxkash/named-entity-recognition-nlp/blob/main/ResearchPaper_bert.pdf) |
| 7 | Histopathological Cancer Detection via Patch-Based CNN | [PDF](https://github.com/omprxkash/histopathological-cancer-detection/blob/main/cancer%20research%20paper.pdf) |
| 8 | Neural Texture Stylization Using Deep Feature Representations | [PDF](https://github.com/omprxkash/texture-model-stylization/blob/master/Neural_Texture_Stylization_Omprakash_2025.pdf) |
| 9 | Cross-Lingual Transfer for Low-Resource NLP | [.tex](https://github.com/omprxkash/multilingual-resource-models/blob/master/paper/main.tex) |
| 10 | AI-Integrated Smart Blood Bank Platform | [paper.tex](papers/blood-bank/paper.tex) |

---

I got tired of losing track of papers. The cycle was always the same: find something interesting on ArXiv, save the tab, forget the tab, re-discover it three weeks later. So I built this.

`ra` is a command-line tool that acts like a research advisor. It searches ArXiv and Semantic Scholar simultaneously, deduplicates the results, and ranks them by relevance. It stores everything locally in a SQLite database so your library is yours — no account, no cloud, no subscription. And when you want more than search results, you can ask Claude to summarize a paper, identify gaps in your literature, or generate a draft review.

## What it does

```
ra search "transformer attention"      # Search ArXiv + S2, ranked by relevance
ra search "machine learning" --save    # Save all results to local library
ra add 1706.03762                      # Save a specific paper by ArXiv ID
ra read 1                              # Full details for paper #1
ra summarize 1                         # Claude summarizes: contributions, limitations
ra gaps "federated learning"           # Claude finds open research questions
ra review "graph neural networks"      # Auto-generate a literature review
ra graph "deep learning"               # Citation network, ranked by PageRank
ra trend "computer vision"             # Publication counts over years (sparkline)
ra dataset "image segmentation"        # Find datasets on HuggingFace + Papers With Code
ra list                                # Browse your library
ra export --format bibtex              # Export as BibTeX / Markdown / JSON
```

## Install

```bash
git clone https://github.com/omprxkash/research-assistant-cli
cd research-assistant-cli
pip install -e ".[dev]"

cp .env.example .env
# add your ANTHROPIC_API_KEY to .env
```

Requires Python 3.11+. The database lives at `~/.ra/library.db` — it's created automatically on first run.

## How it works

```
ra search "topic"
  ├── ArXiv API (Atom XML)
  ├── Semantic Scholar API (JSON REST)
  │
  ├── Deduplicate (DOI match → ArXiv ID cross-ref → fuzzy title match)
  ├── Rank (title overlap 50% + citation count 30% + recency 20%)
  └── Display as Rich table

ra add <arxiv-id>
  ├── Fetch paper + reference list from S2
  ├── Upsert into SQLite (papers, citation_edges)
  └── Auto-link to existing library papers via reference list

ra graph
  ├── Load papers + citation_edges from DB
  ├── Build directed graph (A→B = "A cites B")
  ├── Compute PageRank (α=0.85)
  └── Render ASCII table or Mermaid flowchart

ra summarize 1
  └── Claude prompt → contributions, methodology, limitations → saved to DB
```

## Tech stack

| What | Why |
|---|---|
| Python 3.11 | Type hints, pattern matching, fast stdlib |
| Typer + Rich | Beautiful CLI with no boilerplate |
| SQLAlchemy + SQLite | Local-first, zero config, full relational model |
| httpx | Async HTTP for parallel ArXiv + S2 searches |
| NetworkX | Citation graph + PageRank |
| Anthropic SDK | Claude for summarization and gap analysis |
| pandas | Trend aggregation |

## The non-obvious parts

**Deduplication**: The same paper often appears on both ArXiv and Semantic Scholar with slightly different metadata. I use three passes: exact DOI match, ArXiv ID cross-reference (S2 carries this in `externalIds`), and Jaccard word-set similarity on normalized titles. The threshold is 0.85 — high enough to avoid false merges, low enough to catch title formatting differences.

**Relevance ranking**: `score = 0.5 × title_overlap + 0.3 × log_citations + 0.2 × recency`. Deterministic and reproducible — the same query always gives the same order. The weights are a deliberate editorial choice: relevance over impact over freshness.

**Citation graph**: Directed graph where an edge A→B means "A cites B." Papers with many incoming edges (cited by many other papers) surface to the top via PageRank. The graph auto-densifies: every time you add a paper, its reference list is checked against your library and edges are inserted automatically.

**Gap analysis**: All paper abstracts are sent in a single Claude prompt, not summarized one-by-one. Research gaps only exist relative to the full corpus — you can't identify them by reading papers individually.

## License

MIT
