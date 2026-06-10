# RAG Patterns

Practical patterns for building accurate, scalable, and enterprise-ready Retrieval Augmented Generation systems.

This repository expands the ideas from the article **“Stop Blaming the LLM: RAG Accuracy is a Retrieval Problem”** into reusable architecture assets.

## Pattern Catalog

| Pattern | Purpose |
|---|---|
| Hybrid Search | Combine lexical and semantic retrieval |
| Reranking | Improve result quality before generation |
| Small-to-Big Retrieval | Retrieve precise chunks but provide broader context |
| Query Expansion | Convert vague questions into stronger retrieval queries |
| RAG Evaluation Loop | Continuously measure retrieval and answer quality |

## Repository Structure

```text
hybrid-search/
reranking/
small-to-big-retrieval/
query-expansion/
evaluation-loop/
```

## Operating Principle

RAG accuracy is rarely just an LLM problem. In production systems, answer quality depends heavily on retrieval design, ranking, chunking, metadata, evaluation, and observability.
