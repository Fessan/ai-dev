# PRD: Remove project-development Skill

## Summary
Удалить skill `project-development` из `.claude/skills/`.

## Motivation
Пользователь запросил удалить этот skill из проекта.

## Scope
- Удалить папку `.claude/skills/project-development/` целиком.

## Out of Scope
- Изменения других skills.
- Изменения в правилах использования skills.

## Requirements
- Папка `.claude/skills/project-development/` должна быть удалена.
- В `docs/plans.md` должна быть ссылка на этот PRD.

## Acceptance Criteria
- Папка `.claude/skills/project-development/` отсутствует.
- В `docs/plans.md` добавлена запись о PRD.

## Risks
- Возможные ссылки на `project-development` в документации или правилах.

## Notes
- Проверить наличие ссылок и при необходимости сообщить пользователю.
