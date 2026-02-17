# ANTIGRAVITY SYSTEM DECLARATION

This project enforces:

- aegis-core/GLOBAL_TOKEN_POLICY.md
- aegis-core/UNIFIED_EXECUTOR.md

Adapters may apply based on project type.

All execution must:
- Use diff-only input
- Avoid nested calls
- Produce artifact-only output
## Deployment Rule (Copy Mode)

If this project does not contain `.aegis-core/`:
- Create `.aegis-core/`
- Copy the minimal required files from the upstream `aegis-core` template set
- Create `.aegis-core/VERSION.txt` with source commit hash
- After deployment, treat `.aegis-core/` as read-only

Never duplicate or rewrite the whole policy text into the conversation.
Always reference `.aegis-core/*` files.
## Enforcement Rules

Before any execution:

1. Verify `.aegis-core/VERSION.txt` exists.
2. If missing, STOP and request deployment.
3. Do not proceed without policy validation.

During execution:

- If a nested call is required → STOP.
- If full-project scan is attempted → STOP.
- If diff is insufficient → output NEED_MORE_CONTEXT only.

Never silently fallback to full analysis.
Policy Validation Mode:
- Always output ACTIVE_POLICY_VERSION from VERSION.txt
