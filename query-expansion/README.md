# Query Expansion Pattern

Query Expansion rewrites or expands user questions into multiple stronger retrieval queries.

## When to Use

- Users ask vague or incomplete questions.
- Domain terminology differs across documents.
- You need better recall across synonyms, acronyms, and related concepts.

## Diagram

```mermaid
flowchart LR
    Q[User Query] --> E[Query Expansion]
    E --> Q1[Expanded Query 1]
    E --> Q2[Expanded Query 2]
    E --> Q3[Expanded Query 3]
    Q1 --> R[Hybrid Retrieval]
    Q2 --> R
    Q3 --> R
    R --> C[Context Builder]
    C --> L[LLM]
```
