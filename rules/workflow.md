# Workflow Rules (Source of Truth)

## Mandatory Order
1. Read `INSTRUCTIONS.md` fully.
2. Identify request type and read the matching agent file in `.claude/agents/`.
3. Read guides in `.claude/guides/`.
4. Find stack/run/test commands from real config files.

## Before Any File Changes
- Ask clarifying questions if anything is unclear.
- Provide a mini-plan (5–9 steps) that lists affected files and includes
  "Verification / how we will confirm it works".
- Include the Implementation Checklist from `INSTRUCTIONS.md`.
- Wait for explicit user approval before changing files.
- Exceptions: auto-updating guides, `/init-project`, `/brainstorm`.

## TDD Is Mandatory
1. Write a failing test.
2. Run tests to confirm failure (RED).
3. Write minimal code to pass (GREEN).
4. Run tests to confirm pass.
5. Refactor if needed and re-run tests.

## Agents and Reviews
- Use specialized agents for development, review, security, and secrets.
- After finishing work with `code-developer`, always run `code-reviewer`.

## Guides and Decisions
- Update guides and `DECISIONS.md` when triggers apply (see `INSTRUCTIONS.md`).
