---
name: add-api-endpoint
description: "Trigger this skill when asked to add, write, or implement a new HTTP endpoint to the Flask API backend."
---

# Add API Endpoint Procedure

When this skill is loaded, execute the following numbered steps in strict sequence:

1. **Identify the Blueprint:** Locate the appropriate Flask blueprint (e.g., inside `backend/api/`) where this route belongs.
2. **Define the Route:** Write the route decorator and handler function adhering strictly to the naming conventions of adjacent routes.
3. **Parse Input:** Extract parameters (query args, JSON payloads, headers) using matching existing patterns (e.g., marshmallow schemas or request parsing utilities).
4. **Touch the Store:** Consult the database model or storage repository to query or persist data.
5. **Serialize & Shape Response:** Return JSON data utilizing existing serialization structures or response helper helpers.
6. **Error Handling:** Wrap core steps in matching `try-except` blocks and return appropriate HTTP status codes.
7. **Write a pytest Test:** Draft a corresponding test inside the appropriate testing directory utilizing existing fixtures like `client`.
8. **Verify & Report:** Verbally summarize the changes made and state that the procedure is complete.

## Out of Scope
- This skill **must not** modify frontend components (e.g., React components, assets, styling files).
- This skill **must not** perform database migrations. If a database schema change is needed, stop and notify the user to run a migration skill first.