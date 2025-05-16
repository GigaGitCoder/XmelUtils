# Contribution Guidelines (Руководство по участию)

Thank you for considering contributing to Igor's Utilities! We welcome all types of contributions.

(Спасибо за интерес к проекту! Мы принимаем различные виды участия.)

## How to Contribute (Как участвовать)

### 1. Reporting Issues (Сообщение о проблемах)
- Check existing issues to avoid duplicates
(Проверьте существующие issues во избежание дубликатов)
- Use clear, descriptive titles (e.g., "many_count() returns incorrect value for Unicode characters")
(Используйте понятные заголовки)
- Include: (Укажите:)
  - Python version (Версию Python)
  - Package version (`pip show xmelutils`)
  - Steps to reproduce (Шаги для воспроизведения)
  - Expected vs actual behavior (Ожидаемый и фактический результат)

### 2. Feature Requests (Запросы возможностей)
- Start with "Feature:" prefix (Начните с "Feature:")
- Describe the use case (Опишите сценарий использования)
- Suggest implementation if possible (Предложите реализацию, если возможно)

### 3. Development Setup (Настройка среды)
```bash
git clone https://github.com/GigaGitCoder/XmelUtils.git
cd xmelutils
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows
pip install -e ".[dev]"
```

### 4. Code Style (Стиль кода)
We follow:
(Мы следуем:)
- PEP 8 (with 120-char line length)
- Type hints for new code (Аннотации типов для нового кода)
- Google-style docstrings (Документирование в стиле Google)
```python
def many_count(text: str, chars: str, case_insensitive: bool = False) -> int:
    """Count occurrences of multiple characters in a string.

    Args:
        text: Input string to search in
        chars: Characters to count
        case_insensitive: Whether to ignore case (default: False)

    Returns:
        Total count of all specified characters
    """
```

### 5. Testing (Тестирование)
- Write tests for new features (Пишите тесты для новых возможностей)
- Run tests with: (Запуск тестов:)
```bash
pytest tests/ --cov=xmelutils --cov-report=term-missing
```

### 6. Pull Requests (Запросы на включение)
1. Fork the repository (Сделайте форк репозитория)
2. Create a feature branch (Создайте ветку для изменения):
```bash
git checkout -b fix/issue-123
```
3. Commit messages should follow: (Сообщения коммитов в формате:)
```
feat: add Unicode support to many_count()
fix: correct edge case in character counting
docs: update README with new examples
```
4. Push and open PR (Отправьте изменения и создайте PR)

## Code of Conduct (Правила поведения)
We follow the [Python Community Code of Conduct](https://www.python.org/psf/conduct/). Be kind!

(Мы соблюдаем Кодекс поведения сообщества Python.)

---

**Thank you for your contribution!** (Спасибо за ваш вклад!)  
- IgorXmel (Maintainer)
