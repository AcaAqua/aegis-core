# GLOBAL TOKEN POLICY

## Purpose
Minimize token consumption across all projects.

## Core Rules

1. Single-pass execution only.
2. No nested skill calls.
3. Diff-only processing.
4. No full-project re-scan.
5. Output artifacts only.
6. No verbose explanation.
7. If insufficient context, stop with:
   NEED_MORE_CONTEXT:
   - <required file>

## Execution Model
All tasks must:
- Read only approved inputs
- Complete in one execution
- Avoid multi-step conversational refinement

This policy overrides project-specific behavior.
