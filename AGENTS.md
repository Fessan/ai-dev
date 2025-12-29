# Инструкции для Codex CLI

Этот файл читается Codex CLI автоматически при старте сессии.

## Быстрый старт

1. Прочитай `INSTRUCTIONS.md`
2. Прочитай `context.md` — стек, команды, структура
3. Если неясно — спроси

## Агенты (по запросу)

- `.claude/agents/code-developer.md` — разработка
- `.claude/agents/code-reviewer.md` — ревью
- `.claude/agents/security-auditor.md` — безопасность
- `.claude/agents/secret-scanner.md` — секреты

## Правила (sync from `rules/lite.md`)

- Не предполагай стек без чтения `context.md`
- Простая задача (1-3 файла): уточни → делай
- Сложная задача: мини-план → апрув → делай
- Тесты обязательны для: платежи, auth, данные пользователей
- После изменений обновляй `context.md`
