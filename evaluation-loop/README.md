# RAG Evaluation Loop

A production RAG system needs continuous evaluation across retrieval, context quality, and answer quality.

## Diagram

```mermaid
flowchart TD
    U[User Questions] --> R[Retriever]
    R --> C[Retrieved Context]
    C --> L[LLM]
    L --> A[Answer]
    A --> E[Evaluation]
    C --> E
    E --> M[Metrics]
    M --> I[Improve Chunking / Indexing / Ranking]
    I --> R
```

## Metrics

- Retrieval precision
- Retrieval recall
- Context relevance
- Groundedness
- Faithfulness
- Answer relevance
- Citation accuracy
