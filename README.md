# Personal Engineering Playbook (OpenCode Skill)

Reusable OpenCode skill for hackathons and personal software projects. Version 2
incorporates documented workflow patterns and evaluation scenarios.

This repository is an **OpenCode skill**, not a standalone application. It contains
instructions, references, templates, and evaluation scenarios that OpenCode loads
on demand. It does not install dependencies, run services, or modify a project by
itself.

## What it does

The skill acts as a senior engineering partner for:

- Project discovery and scoping
- Architecture and implementation planning
- Backend (Python/FastAPI/PostgreSQL) and frontend (React/TypeScript/Vite) work
- UI component and template selection
- Security, accessibility, testing, and review
- Debugging and minimal fixes
- Optional, evidence-based AI/ML decisions
- Documentation and handoff

## Features and capabilities

- Progressive disclosure: concise core rules in `SKILL.md`, detailed guidance in
  `references/`.
- Approval gates before substantial implementation.
- Default stack with explicit justification requirements.
- Security and accessibility treated as baseline requirements.
- Templates for project briefs and implementation plans.
- Evaluation scenarios for manual skill validation.

## Repository structure

```text
personal-engineering-playbook/
├── SKILL.md
├── references/
├── templates/
├── evaluations/
├── README.md
├── LICENSE
├── CHANGELOG.md
└── .gitignore
```

## Installation

### Project-local

```text
.opencode/skills/personal-engineering-playbook/
```

### User-global

```text
~/.config/opencode/skills/personal-engineering-playbook/
```

OpenCode also supports compatibility locations such as `.claude/skills` and
`.agents/skills`. See the OpenCode Skills documentation for the full discovery
rules.

After installation, ask OpenCode to use the skill by name:

> Use the personal-engineering-playbook skill. Inspect this repository, identify
> the project mode, and prepare discovery questions and a proposed implementation
> plan. Do not make major changes until I approve the plan.

## Usage examples

- "Use the playbook. I have 5 days to build a small event registration app with
  React, FastAPI, and PostgreSQL. Help me scope it."
- "Use the playbook. Audit this repository for architecture, broken flows, missing
  tests, and security risks. Do not edit files."
- "Use the playbook. The registration endpoint accepts duplicate registrations.
  Reproduce the issue, fix it, and verify the behavior."

## Supported workflows

See `SKILL.md` for the full workflow. Evaluation scenarios are in
`evaluations/README.md`.

## Defaults

- Backend: Python + FastAPI + PostgreSQL.
- Frontend: React + TypeScript + Vite.
- UI choices: 21st.dev, shadcn/ui, or GitHub starters when appropriate.
- AI/ML: optional and problem-driven.
- Testing: Pytest/HTTPX, Vitest/React Testing Library, Playwright where useful.

The skill is a set of instructions, not an installed dependency bundle. It does not
automatically install packages or verify external services.

## Research and validation

The workflow was informed by:

- OpenCode's official Skills documentation.
- `obra/superpowers` development workflow.
- Anthropic's Agent Skills authoring guidance.

See `references/influences-and-adaptation.md` for what was adapted and what was
deliberately not copied. Run the scenarios in `evaluations/README.md` in OpenCode
before treating the skill as proven.

## Contributing

1. Keep `SKILL.md` concise; put detailed guidance in `references/`.
2. Preserve relative paths and OpenCode skill conventions.
3. Do not commit secrets, credentials, personal data, or machine-specific paths.
4. Update `CHANGELOG.md` for meaningful changes.
5. Run the evaluation scenarios in `evaluations/README.md` after material changes.

## License

MIT. See `LICENSE`.
