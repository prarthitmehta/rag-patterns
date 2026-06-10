# Reranking Pattern

Reranking improves the quality of retrieved chunks before sending context to the LLM.

## When to Use

- Initial search returns many moderately relevant documents.
- The top results are noisy.
- You need higher answer precision without increasing prompt size.

## Diagram

```mermaid
flowchart LR
    Q[User Query] --> S[Initial Search]
    S --> T[Top 20-50 Candidates]
    T --> R[Cross-Encoder / Reranker]
    R --> B[Best 3-8 Chunks]
    B --> L[LLM]
    L --> A[Answer with Sources]
```

## Implementation Notes

- Retrieve broad, then rerank narrow.
- Track reranker latency separately.
- Evaluate reranked precision against baseline retrieval.
