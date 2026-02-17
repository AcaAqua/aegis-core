# ETL ADAPTER

## Scope
For data transformation tasks.

## Rules
- Preserve schema integrity.
- Enforce numeric type correctness.
- Do not reprocess entire dataset.

## Optimization
- Apply transformation only to diff-scope changes.
- Avoid full table regeneration.

Execution must remain single-pass.
