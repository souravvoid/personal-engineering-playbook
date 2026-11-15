# Frontend standards — React and TypeScript

## Defaults
- React + TypeScript; Vite for a lightweight SPA unless the project needs another framework.
- Use strict TypeScript where practical.
- Keep dependencies minimal and aligned with the existing repository.

## Component design
- Prefer small components with clear responsibilities.
- Separate reusable UI primitives from feature-specific components.
- Keep business logic out of deeply nested JSX.
- Avoid premature global state. Use local state first; add a state library only when complexity justifies it.
- Define API types and handle loading, empty, error, success, and disabled states.

## Data and forms
- Validate user input on both client and server; server validation is authoritative.
- Handle request cancellation/stale responses where relevant.
- Avoid duplicating server state unnecessarily.
- Do not store secrets in frontend environment variables; client-exposed variables are public.

## UI libraries
- Consider shadcn/ui for a consistent project-owned component foundation.
- Consider 21st.dev for individual components/patterns after inspecting source, dependencies, accessibility, and license.
- Consider GitHub starters for project scaffolding after reviewing maintenance, license, dependency versions, scripts, and security.
- Do not stack multiple component libraries without a clear need.

## Accessibility and performance
- Use semantic elements, labels, keyboard support, visible focus, and sufficient contrast.
- Respect reduced-motion settings.
- Use appropriate image sizing/lazy loading.
- Avoid unnecessary rerenders and large dependencies; profile before optimizing.

## Verification
Run lint/typecheck/tests/build scripts available in the repository. Test meaningful interactions, forms, navigation, and error/loading states.
