# Core Rules (Source of Truth)

This file defines the shared baseline rules for all assistants.

## Identity and Entry
- This repo is AI-first; follow `INSTRUCTIONS.md` as the primary workflow.
- Always use the appropriate agent from `.claude/agents/` for the task.
- Always state which agent and which skills are in use.

## Context and Evidence
- Do not assume structure, stack, or commands without reading files.
- Prefer `rg` for search and file discovery when possible.
- If information is missing, ask questions and wait for answers.

## Safety and Changes
- Do not use destructive commands unless explicitly requested.
- Never revert unrelated changes made by the user.
