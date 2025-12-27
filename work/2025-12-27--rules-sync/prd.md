# PRD: Rules Sync for AI Assistants

## Summary
Ввести единый источник правил в `rules/` (Markdown) и синхронизировать их в файлы ассистентов: `AGENTS.md`, `INSTRUCTIONS.md`, `CLAUDE.md`, `.cursorrules`, `.antigravity/rules.md`.

## Motivation
Снизить дублирование правил, обеспечить консистентность между разными ассистентами (Codex, Claude, Cursor, Antigravity).

## Scope
- Создать `rules/` как источник истины для общих правил.
- Добавить синхронизацию правил в целевые файлы.
- Обновить README с инструкцией по синхронизации.

## Out of Scope
- Автоматический CLI-инструмент (можно добавить позже).
- Изменение текущих бизнес-правил проекта.

## Requirements
- `rules/core.md` и `rules/workflow.md` содержат канонические правила.
- Целевые файлы обновлены и отражают эти правила.
- README содержит инструкцию по синхронизации.

## Acceptance Criteria
- `rules/` существует и содержит правила.
- `AGENTS.md`, `INSTRUCTIONS.md`, `CLAUDE.md`, `.cursorrules`, `.antigravity/rules.md` согласованы по смыслу.
- README описывает, как обновлять правила.

## Risks
- Дублирование конфликтующих правил в существующих файлах.

## Notes
- Приоритет: ясность и краткость; без потери обязательных шагов из `INSTRUCTIONS.md`.
