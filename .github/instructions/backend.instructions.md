---
applyTo: "backend/**/*.py"
---

# Backend Instructions

Use Flask patterns consistent with this repository.

- Keep API endpoints in Flask Blueprints, matching `backend/api/users.py` conventions.
- Return JSON responses with `jsonify(...)` and explicit status-code tuples.
- For user data operations, use the shared in-memory `store` from `backend/store.py`.
- Reuse existing access patterns (`store.create`, `store.get`, `store.list_all`) instead of introducing new persistence layers.
- Serialize dataclass models with `asdict(...)` for API responses.
- Preserve existing route naming, module layout, and import style.
- Keep changes minimal and scoped to the requested backend behavior.
