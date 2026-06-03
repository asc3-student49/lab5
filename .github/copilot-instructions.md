# Repository-Wide Copilot Instructions

This repository is a small Flask + pytest project used for configuration experiments. Keep suggestions minimal, consistent with existing patterns, and scoped to the user's request.

## Tech stack and style

- Backend framework is Flask. Do not propose FastAPI, Django, or other frameworks unless explicitly requested.
- Tests use pytest. Prefer pytest fixtures and simple function-based tests; do not introduce unittest-style classes unless asked.
- Keep code straightforward and consistent with existing files.

## Backend conventions (`backend/`)

- Follow the current API pattern in `backend/api/users.py`: Flask Blueprint routes, `jsonify` responses, and status-code tuples.
- Use the in-memory `store` from `backend/store.py` for user data operations.
- Serialize dataclasses using `asdict` where appropriate, matching existing endpoint behavior.
- Reuse existing naming conventions and module structure.

## Testing conventions (`tests/`)

- Add or update tests in `tests/test_users.py` unless asked to create a new test module.
- Reuse the existing `client` fixture pattern.
- Keep test names in `test_<behavior>` style and assertions direct and readable.

## Migration conventions (`migrations/`)

- Treat migrations as append-only.
- Never modify previously committed migration files.
- For schema changes, propose a new numbered migration file using `NNNN_short_description.py` format.

## File safety and scope

- Do not edit generated artifacts under `build/` or `generated/` unless explicitly asked.
- Do not hand-edit lockfiles as part of normal feature work.
- Prefer targeted edits over broad refactors.

## When implementing changes

- Update only files relevant to the request.
- If behavior changes, include or update pytest coverage.
- Preserve existing public behavior unless the prompt explicitly requests behavior changes.
