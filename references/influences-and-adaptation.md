# Engineering workflow references and how this playbook adapts them

This file records the public references used to improve the playbook. It is not an endorsement of copying another project's entire methodology.

## 1. OpenCode Skills documentation
https://opencode.ai/docs/skills

Adapted:
- Use a directory containing `SKILL.md` and nearby references/templates.
- Keep the skill discoverable through a clear description.
- Keep the skill ID aligned with its lowercase kebab-case directory name.
- Link supporting files explicitly because they are not automatically loaded.
- OpenCode global location: `~/.config/opencode/skills/<skill-id>/SKILL.md`.
- Project-local location: `.opencode/skills/<skill-id>/SKILL.md`.

## 2. obra/superpowers
https://github.com/obra/superpowers

Useful ideas adapted:
- Clarify and validate the problem before implementation.
- Get design approval before writing a substantial implementation.
- Break work into small, verifiable tasks.
- Use RED-GREEN-REFACTOR TDD when a meaningful test can be written.
- Separate debugging, code review, and branch completion into explicit activities.
- Review for both requirement compliance and code quality.

Not copied wholesale:
- This playbook does not require subagents, worktrees, or a rigid multi-hour workflow for every small hackathon task. Those add overhead unless the repository, agent setup, and task justify them.

## 3. Anthropic Agent Skills authoring best practices
https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices

Useful ideas adapted:
- Keep the main skill concise; use progressive disclosure for detailed references.
- Give the agent freedom when several solutions are reasonable and precise guardrails when an operation is fragile.
- Test the skill against representative tasks and refine from actual failures.
- Keep metadata specific about what the skill does and when to use it.

These are general skill-authoring ideas. OpenCode's own documentation remains authoritative for OpenCode-specific paths and behavior.

## Adaptation rule

For every borrowed practice, ask:
1. Does it solve a real failure mode in the user's projects?
2. Is it compatible with OpenCode and the selected model/tools?
3. Does it help a hackathon project without creating disproportionate overhead?
4. Can the agent verify that it followed the practice?

If not, do not add it.
