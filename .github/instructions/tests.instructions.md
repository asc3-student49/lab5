---
applyTo: "tests/**/*.py"
---

# Test Instructions

Use pytest patterns consistent with this repository.

- Write tests in pytest style using simple function-based tests.
- Reuse existing fixtures, especially the shared `client` fixture pattern in `tests/test_users.py`.
- Keep test names in `test_<behavior>` format.
- Keep assertions direct and readable.
- Add or update tests in `tests/test_users.py` unless explicitly asked to create a new test module.
- Do not introduce unittest-style classes.
- Do not introduce mocking frameworks unless explicitly requested.
- Keep tests focused on observable behavior of endpoints and store interactions.
