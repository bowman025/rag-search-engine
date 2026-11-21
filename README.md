# Retrieval-Augmented Generation (RAG) Search Engine

A Python search engine and RAG pipeline built from scratch as part of Boot.dev's **Learn Retrieval Augmented Generation** course. Rather than relying on high-level abstractions like LangChain, this project implements core information retrieval, ranking, evaluation, and LLM-augmentation mechanics directly in Python.

## Core Concepts & Features

- **Text Preprocessing:** Normalization, punctuation removal, tokenization, stop-word filtering, and Porter stemming (`nltk`).
- **Keyword Search:** Custom inverted index with disk serialization, TF-IDF weighting, and BM25 ranking with field-level boosts.
- **Semantic & Hybrid Search:** Context-preserving chunking, dense vector embeddings, cosine similarity search, and hybrid keyword/semantic score fusion.
- **Optimization & Evaluation:** LLM-assisted query rewriting, candidate reranking, and precision/recall evaluation metrics.
- **Augmented, Agentic & Multimodal RAG:** Grounded answer synthesis, iterative agentic search loops, and multimodal retrieval across text and images.

## Project Structure

```text
├── cli/
│   ├── lib/      # Core search engine logic (inverted index, BM25, embeddings, reranking)
│   └── *.py      # CLI entry points for keyword, semantic, hybrid, and RAG workflows
└── pyproject.toml
```

## Dataset Note

The dataset files (`data/*.json`) used during the course are intentionally excluded via `.gitignore` as they are provided through Boot.dev's course environment. The search and indexing modules expect a JSON array of records structured like:

```json
[
  {
    "id": 1,
    "title": "Example Title",
    "description": "Text content indexed for keyword and semantic search..."
  }
]
```

## Acknowledgments

Completed as part of [Learn Retrieval Augmented Generation](https://www.boot.dev/courses/learn-retrieval-augmented-generation) by Isaac Flath on Boot.dev.
