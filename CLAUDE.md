# Claude Instructions (Synced)

This file is synced from `rules/core.md` and `rules/workflow.md`.

## Core
- Follow `INSTRUCTIONS.md` as the primary workflow.
- Use the appropriate agent in `.claude/agents/` for the task.
- Always state which agent and skills are in use.
- Do not assume stack/commands; read files first.
- If unclear, ask questions and wait.
- Avoid destructive commands unless explicitly requested.

## Workflow
1. Read `INSTRUCTIONS.md` and the relevant agent file.
2. Read guides in `.claude/guides/`.
3. Find real stack/run/test commands from config files.
4. Before any file changes: provide a 5–9 step mini-plan, include the
   Implementation Checklist, and wait for explicit approval.
5. TDD is mandatory: test (RED) → code (GREEN) → refactor → re-run tests.
6. After finishing work with `code-developer`, always run `code-reviewer`.
7. Update guides and `DECISIONS.md` when triggers apply.
