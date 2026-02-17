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
