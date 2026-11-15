# Skill evaluation scenarios

Run these scenarios manually in OpenCode after installing or materially changing the skill. Evaluate behavior, not whether the agent repeats the instructions.

A scenario passes only when the expected behavior is observable. Record model/version, repository fixture, commands run, outcome, and misses.

## Scenario 1 — New hackathon MVP
Prompt:
> Use the personal engineering playbook. I have 5 days to build a small event registration app with React, FastAPI, and PostgreSQL. Help me scope it.

Expected:
- Identifies the critical user journey and deadline.
- Separates must-have from optional features.
- Does not add AI/ML without a real requirement.
- Proposes a small architecture, acceptance criteria, and test plan.
- Waits for approval before substantial implementation.

## Scenario 2 — Existing repository audit
Prompt:
> Use the playbook. Audit this repository for architecture, broken flows, missing tests, and security risks. Do not edit files.

Expected:
- Inspects existing conventions, manifests, tests, Git status, and project structure.
- Reports findings with evidence and severity.
- Does not modify files or claim tests were run when they were not.
- Does not recommend a rewrite merely to match the default stack.

## Scenario 3 — Bug fix
Prompt:
> Use the playbook. The registration endpoint accepts duplicate registrations. Reproduce the issue, fix it, and verify the behavior.

Expected:
- Finds the relevant endpoint, model, and persistence constraints.
- Adds or identifies a regression test.
- Confirms the test fails before the fix when feasible.
- Implements a minimal fix, including database integrity protection if appropriate.
- Reruns relevant tests and reports actual results.

## Scenario 4 — Frontend design
Prompt:
> Use the playbook. Build a responsive landing page for this product using the existing project setup.

Expected:
- Inspects existing dependencies and design conventions first.
- Chooses shadcn/ui, 21st.dev, or neither based on actual needs.
- Does not add competing component libraries unnecessarily.
- Covers responsive, loading/error/empty states where relevant, semantic HTML, and keyboard interaction.
- Runs available lint, typecheck, tests, and build.

## Scenario 5 — Optional ML decision
Prompt:
> Use the playbook. I want to add AI to this CRUD application because it looks more impressive.

Expected:
- Challenges the premise instead of adding an unnecessary model.
- Asks what user problem AI solves and compares a simpler baseline.
- If AI is justified, defines data, evaluation, failure handling, privacy, and cost considerations.
