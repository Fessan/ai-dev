# ai-dev (Lite)

Лёгкий шаблон для быстрой AI-First разработки MVP.

Работает с **Claude Code**, **Codex CLI**, **Cursor**, **Antigravity**.

## Особенности

- **Быстрый старт**: 4 вопроса вместо 15
- **1 файл контекста**: `context.md` вместо 5 guides
- **Гибкие тесты**: обязательны только для критичного кода
- **Агенты и скиллы**: доступны по запросу

## Быстрый старт

```bash
git clone <repo-url> my-project
cd my-project
```

В Claude Code или Codex CLI:

```
/init-project
```

Начать работу:

```
"Хочу добавить авторизацию"
```

## Структура

```
project/
├── INSTRUCTIONS.md      # Точка входа для ИИ
├── AGENTS.md            # Для Codex CLI
├── CLAUDE.md            # Для Claude Code
├── context.md           # Контекст проекта (стек, команды)
├── TODO.md              # Список задач
├── .cursorrules         # Для Cursor
│
├── rules/
│   └── lite.md          # Источник правил
│
├── .claude/
│   ├── agents/          # Агенты (по запросу)
│   ├── skills/          # Скиллы (по запросу)
│   └── commands/
│       └── init-project.md
│
└── .antigravity/
    └── rules.md
```

## Workflow

```
Запрос → Уточнение (если надо) → Код → Тесты (если критично)
```

### Простая задача (1-3 файла)
Уточни → делай

### Сложная задача
Мини-план → апрув → делай

## Правила

### Тесты
- **Обязательны**: платежи, auth, данные пользователей
- **Опционально**: CRUD, UI, утилиты

### Принципы
- **KISS** — простота
- **YAGNI** — не добавляй "на будущее"
- **DRY** — не дублируй

## Агенты (по запросу)

| Агент | Назначение |
|-------|------------|
| `code-developer` | Разработка |
| `code-reviewer` | Ревью |
| `security-auditor` | Безопасность |
| `secret-scanner` | Секреты |

## Скиллы

В `.claude/skills/` доступна библиотека навыков:
- brainstorming, writing-plans
- test-driven-development
- systematic-debugging
- context engineering skills
- и другие

Используй по необходимости.

## Универсальность

| Инструмент | Читает |
|------------|--------|
| Claude Code | `CLAUDE.md` + `.claude/` |
| Codex CLI | `AGENTS.md` + `INSTRUCTIONS.md` |
| Cursor | `.cursorrules` |
| Antigravity | `.antigravity/rules.md` |

## Rules Sync

Источник правил: `rules/lite.md`

Синхронизируется в:
- `CLAUDE.md`
- `AGENTS.md`
- `.cursorrules`
- `.antigravity/rules.md`

## Лицензия

Apache 2.0
