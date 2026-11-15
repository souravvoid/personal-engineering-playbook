# Backend standards — Python and FastAPI

## Defaults
- Python + FastAPI; Pydantic for validation; SQLAlchemy 2.x when ORM use is justified; Alembic for migrations; PostgreSQL for relational data.
- Prefer `uv` for new Python projects unless the environment/repository already standardizes on another tool.
- Use type hints and clear module boundaries.

## Structure
Keep API routing, business rules, persistence, configuration, and schemas separate when project complexity warrants it. Route handlers should orchestrate, not contain large blocks of business logic. Avoid creating layers that merely forward calls.

## API behavior
- Define request/response schemas explicitly.
- Use correct HTTP methods/status codes and consistent error shapes.
- Validate all input server-side.
- Keep secrets and internal exception details out of responses.
- Document auth, pagination, filtering, and important error cases.
- Use dependency injection for shared resources where it improves testability.

## Database
- Use migrations for schema changes.
- Use transactions for atomic multi-step writes.
- Add constraints and indexes based on integrity and query patterns.
- Use timezone-aware timestamps.
- Avoid raw SQL string concatenation; parameterize queries.
- Test migration paths and database-dependent behavior when feasible.

## Reliability
- Set timeouts for external calls.
- Handle expected network/service failures explicitly.
- Use retries only for transient failures and only when operations are safe to retry.
- Do not swallow exceptions or return success-shaped responses for failures.
- Add structured logging without credentials, tokens, or sensitive payloads.

## Before handoff
Run the project's formatter/linter, type checks if configured, unit tests, API tests, and build/startup checks that are available. Report what did and did not run.
