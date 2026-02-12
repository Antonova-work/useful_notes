## Как создать виртуальное окружение (venv)

Виртуальное окружение позволяет изолировать зависимости конкретного проекта, чтобы они не конфликтовали с системными пакетами.

### 1. Через Терминал (Универсальный способ)

Этот метод работает везде и не зависит от IDE.

 * Создание:
   ```bash
   python3 -m venv .venv
   ```

 * Активация:
   * Linux / macOS:
     ```bash
     source .venv/bin/activate
     ```

   * Windows:
     ```bash
     .venv\Scripts\activate
     ```

 * Деактивация:
   ```bash
   deactivate
   ```

### 2. Через PyCharm (Графический интерфейс)

Самый быстрый способ для разработки в IDE.

 * Откройте Settings (Ctrl+Alt+S).
 * Перейдите в Project: [Имя_Проекта] > Python Interpreter.
 * Нажмите Add Interpreter > Add Local Interpreter...
 * Выберите Virtualenv Environment:
   * Environment: Generate new
   * Location: Путь к папке .venv внутри вашего проекта.
   * Base Python: Путь к установленному в системе Python (например, /usr/bin/python3).
 * Нажмите OK.
   
### 3. Важные советы
 * .gitignore: Всегда добавляй папку .venv/ в файл .gitignore, чтобы не загружать мегабайты лишних файлов на GitHub.
 * requirements.txt: Чтобы другие могли установить твои библиотеки, используй команду:
   pip freeze > requirements.txt
