# Tests

Здесь хранятся все тесты проекта.

## Структура

Структура тестов должна зеркалить структуру `src/`:

```
src/
├── auth/
│   ├── user.py
│   └── jwt.py
├── api/
│   └── routes.py
└── utils/
    └── helpers.py

tests/
├── auth/
│   ├── test_user.py
│   └── test_jwt.py
├── api/
│   └── test_routes.py
└── utils/
    └── test_helpers.py
```

## TDD обязателен

**Всегда:** тест → код (RED-GREEN-REFACTOR)

1. Напиши **падающий тест**
2. Запусти - убедись что **падает** (RED)
3. Напиши **минимальный код**
4. Запусти - убедись что **проходит** (GREEN)
5. Рефактори если нужно (REFACTOR)

## Запуск тестов

Команда запуска указана в `.claude/guides/architecture.md`.

Обычно:

**Python:**
```bash
pytest
pytest tests/
pytest tests/test_file.py
pytest tests/test_file.py::test_function
```

**JavaScript/TypeScript:**
```bash
npm test
npm test -- tests/file.test.ts
```

## Покрытие

Стремись к покрытию минимум 80%.

**Python:**
```bash
pytest --cov=src tests/
```

**JavaScript/TypeScript:**
```bash
npm test -- --coverage
```

## Типы тестов

### Unit Tests
Тестируют отдельные функции/классы в изоляции.

### Integration Tests
Тестируют взаимодействие между компонентами.

### E2E Tests (если нужны)
Тестируют весь flow от начала до конца.

## Принципы

- **Независимость:** тесты не должны зависеть друг от друга
- **Повторяемость:** тест должен давать один и тот же результат
- **Быстрота:** тесты должны работать быстро
- **Читаемость:** тест должен быть понятен как документация

## Примеры

### Python (pytest)

```python
def test_user_creation():
    # Arrange
    user_data = {"email": "test@example.com", "name": "Test"}

    # Act
    user = create_user(user_data)

    # Assert
    assert user.email == "test@example.com"
    assert user.name == "Test"
```

### JavaScript/TypeScript (jest)

```typescript
test('creates user', () => {
  // Arrange
  const userData = { email: 'test@example.com', name: 'Test' };

  // Act
  const user = createUser(userData);

  // Assert
  expect(user.email).toBe('test@example.com');
  expect(user.name).toBe('Test');
});
```

## Тестовые данные

Используй фикстуры/моки для тестовых данных, не хардкодь.

**Python:**
```python
@pytest.fixture
def user():
    return User(email="test@example.com", name="Test")

def test_something(user):
    # используй user fixture
    assert user.email == "test@example.com"
```

**JavaScript:**
```typescript
const mockUser = { email: 'test@example.com', name: 'Test' };
```

## См. также

- `.claude/guides/patterns.md` - стандарты тестирования
- `/test` - команда для запуска тестов
- `/dev` - разработка с TDD
