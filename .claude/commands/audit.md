# /audit

Запустить security audit (OWASP Top 10).

## Описание

Запускает агента `security-auditor` для проверки безопасности.

## Использование

```
/audit
```

Проверит весь проект.

Или конкретные файлы:
```
/audit src/auth/ src/api/
```

## Что проверяет

- OWASP Top 10 (2021)
- Hardcoded secrets
- SQL/NoSQL/Command injection
- XSS, CSRF
- Broken authentication
- Security misconfiguration
- И другие уязвимости

## Output

```markdown
## Security Audit Report

### 🔴 CRITICAL Vulnerabilities
1. **SQL Injection**
   - OWASP: A03:2021
   - Файл: src/db.py:45
   - Fix: Use parameterized queries

### 🟡 IMPORTANT Issues
1. **Weak password policy**
   - OWASP: A07:2021
   - Рекомендация: Require 12+ chars

### ✅ Good Practices
- HTTPS enforced
- JWT tokens properly validated

### Overall Rating
🟡 MODERATE - fix important issues before production
```

## Когда запускать

- Перед релизом
- После реализации фич с user input
- После реализации authentication/authorization
- Периодически (раз в месяц)

## См. также

- `.claude/agents/security-auditor.md` - описание агента
- `/secrets` - проверка hardcoded secrets
- `/review` - code review
