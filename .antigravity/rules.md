# Antigravity Rules (Synced)

Synced from `rules/lite.md`.

## Quick Start
1. Read `context.md` for stack, commands, structure
2. If unclear, ask and wait
3. Do

## Boundaries

### ✅ Always
- Read `context.md` before work
- Check existing code before changes
- Validate inputs
- **Number questions** — so user can reply with just a number
- **Show agent/skill** — state which agent and skill you're using

### ⚠️ Ask first
- Config changes
- Adding dependencies
- Deleting files

### 🚫 Never
- Hardcode secrets
- Commit `.env`
- Assume stack without reading files

## Rules
- Simple task (1-3 files): clarify → code
- Complex task: mini-plan → approval → code
- Tests required for: payments, auth, user data

## Additional Context
- `.claude/agents/*.md` — agents (TDD, review, security)
- `.claude/skills/*/SKILL.md` — skills library

## Principles
- **KISS** — simplicity first
- **YAGNI** — don't add "for the future"
- **DRY** — don't repeat

## Auto-update
Update `context.md` after significant changes.
