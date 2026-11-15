# Testing and verification guidelines

## Strategy
Test behavior and risk, not implementation details. Start with the highest-value user journeys and failure modes.

## Backend
- Unit tests for business rules and edge cases.
- API tests for valid/invalid payloads, auth, authorization, missing resources, and expected failures.
- Database tests for constraints, transactions, and migrations when relevant.
- Use isolated test data and controlled dependencies.

## Frontend
- Component tests for meaningful behavior.
- Test forms, validation, navigation, loading/empty/error states, and accessibility-relevant interactions.
- Use browser end-to-end tests for critical journeys when practical.

## Integration
Verify frontend/backend contracts, persistence, CORS, auth, environment setup, and error handling.

## Test hygiene
- Tests must be deterministic and independent.
- Avoid relying on production services or real credentials.
- Do not weaken assertions just to get a green run.
- Fix the underlying defect rather than hiding it.
- Distinguish skipped tests from passed tests.

## Reporting
List commands run and actual outcomes. If checks could not run, explain why. Never claim “fully tested” without defining the scope.
