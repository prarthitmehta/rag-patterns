# Small-to-Big Retrieval Pattern

Retrieve small chunks for precision, then expand to larger parent sections for complete context.

## When to Use

- Small chunks improve matching but lose surrounding meaning.
- Long policies, SOPs, contracts, manuals, or architecture docs need contextual expansion.

## Diagram

```mermaid
flowchart LR
    Q[User Query] --> S[Small Chunk Retrieval]
    S --> M[Matched Chunk]
    M --> P[Parent Section / Document]
    P --> C[Context Assembly]
    C --> L[LLM]
    L --> A[Grounded Answer]
```

## Implementation Notes

- Store parent-child relationships during ingestion.
- Retrieve at chunk level, answer with section-level context.
- Avoid sending entire documents unless needed.
