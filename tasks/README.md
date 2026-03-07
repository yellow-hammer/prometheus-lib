# Задачи (tasks)

| Задача                     | Файл          | Описание                                                                                                                                 |
|----------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Установка зависимостей** | `install.os`  | `opm install --dev -l` — ставит зависимости в `oscript_modules/` (в т.ч. для разработки: 1testrunner, asserts, coverage, 1commands, fs). |
| **Сборка**                 | `build.os`    | `opm build --out out` — собирает пакет в .ospx (файл в каталоге `out/`).                                                                 |
| **Тесты**                  | `test.os`     | Запуск тестов (1testrunner по каталогу `tests/`). Отчёт в `out/tests.xml`.                                                               |
| **Покрытие**               | `coverage.os` | Тесты с замером покрытия; отчёты в `out/` (Generic, Cobertura, stat.json).                                                               |

Рекомендуемый порядок после клонирования:

```bash
opm run install # или: opm install --dev -l
opm run test
```

Покрытие (требуется пакет coverage):

```bash
opm run coverage
```

Команда `opm test` из корня пакета запускает `tasks/test.os`.
