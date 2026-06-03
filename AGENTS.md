# Agent Behavioral Guidance & Guardrails

## 1. Directory Constraints & Exclusions
- **Off-Limits Directories:** The agent must NEVER directly edit, overwrite, or delete files inside the `migrations/` directory.
- **Build Artifacts Protection:** Under no circumstances should the agent modify build files or package lockfiles. This includes but is not limited to:
  - `build/`
  - `generated/`
  - `node_modules/`
  - `package-lock.json`

## 2. Pre-Action Verification Rules
- **Schema & Model Changes:** Before proposing or executing any database schema, model, or serializer changes, the agent must explicitly state whether a new migration file is required.

## 3. Autonomous Execution Scope Discipline
- **Change Threshold:** If any proposed change requires modifications that span more than two top-level directories, the agent MUST immediately pause and request explicit user confirmation before writing or modifying code.

## 4. Migration Guardrail
- Committed migrations are strictly append-only. To implement schema changes, the agent must propose a new, sequentially numbered migration file instead of editing existing migration files (such as `0002_add_email.py`).
