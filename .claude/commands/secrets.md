# /secrets

Проверка на hardcoded secrets перед коммитом.

## Описание

Запускает агента `secret-scanner` для поиска hardcoded secrets.

## Использование

Проверить staged файлы:
```
/secrets
```

Проверить конкретные файлы:
```
/secrets src/config.py src/auth.py
```

## Что ищет

- API keys (AWS, GitHub, Slack, etc.)
- Passwords
- Database credentials
- Private keys
- OAuth secrets
- JWT secrets
- Telegram bot tokens

## Output

```markdown
## Secret Scan Report

Scanned: 5 files
Secrets found: 2

### 🔴 FOUND SECRETS (BLOCKING)

1. **API Key**
   - File: src/config.py:15
   - Match: `AKIAIOSFODNN7EXAMPLE`
   - Action: REMOVE, use env var

### Verdict
❌ COMMIT BLOCKED - remove secrets first
```

## Когда запускать

- **Перед каждым коммитом** (автоматически)
- При ревью кода
- Перед пушем в репозиторий

## Что делать если нашёл secret

1. НЕ коммить
2. Убрать secret из кода
3. Добавить в .env (и .env в .gitignore)
4. Обновить .env.example с placeholder
5. Ротировать secret если уже был в git истории

## См. также

- `.claude/agents/secret-scanner.md` - описание агента
- `/audit` - security audit
