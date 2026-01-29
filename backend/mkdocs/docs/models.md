# Data Models

## Task Model (SQLAlchemy)

Fields:
- `id`: integer, primary key
- `title`: string
- `description`: string
- `status`: string (`TODO`, `IN_PROGRESS`, `DONE`)
- `created_at`: datetime
- `updated_at`: datetime

## Pydantic Schemas

### TaskCreate
- `title`: str
- `description`: str | None

### TaskUpdate
- `title`: str | None
- `description`: str | None
- `status`: str | None

### TaskOut
- `id`: integer, primary key
- `title`: string
- `description`: string
- `status`: string (`TODO`, `IN_PROGRESS`, `DONE`)
- `created_at`: datetime
- `updated_at`: datetime
