# GET /tasks

## Overview

Retrieves the full list of tasks stored in the database.
Tasks are returned in **descending order of ID**, meaning the most recently created tasks appear first.

This endpoint does **not** require authentication.

---

## Endpoint

```
GET /tasks
```

---

## Response

### Status codes

| Code | Meaning |
|------|---------|
| 200  | Successful retrieval of tasks |

### Response body

A JSON array of `TaskOut` objects:

```json
[
  {
    "id": 1,
    "title": "Buy groceries",
    "description": "Milk, eggs, bread",
    "status": "TODO",
    "created_at": "2025-01-10T14:22:00Z",
    "updated_at": "2025-01-10T14:22:00Z"
  }
]
```

---
