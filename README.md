# Job Market Analyzer

Учебный проект для анализа рынка вакансий. Сейчас реализована минимальная
точка входа: программа выводит сообщение `Job Market Analyzer запущен`.
Сбор и анализ вакансий пока не реализованы.

## Окружение

Использован Python **3.14.0**. Дополнительные библиотеки пока не нужны.

Все команды ниже выполняются в терминале **PowerShell**, из корня проекта —
папки, где находятся `main.py`, `README.md` и `.gitignore`.

```powershell
cd "C:\Users\xmg16\OneDrive\Документы\ChatGPT\Job Market Analyzer"
```

Виртуальное окружение `Job_Market_Analyzer-env` уже создано локально.
На новом компьютере или после удаления окружения его нужно создать заново:

```powershell
python -m venv Job_Market_Analyzer-env
```

Активировать окружение и проверить версию Python:

```powershell
.\Job_Market_Analyzer-env\Scripts\Activate.ps1
python --version
```

## Запуск

С активированным окружением:

```powershell
python main.py
```

Ожидаемый вывод:

```text
Job Market Analyzer запущен
```

Можно запустить программу без активации, указав Python из окружения:

```powershell
.\Job_Market_Analyzer-env\Scripts\python.exe main.py
```

## Проверка импорта

```powershell
python -c "import main"
```

Команда должна завершиться без вывода. Функция `main()` вызывается только
при прямом запуске файла благодаря условию `if __name__ == "__main__":`.

## Git и локальные файлы

`.gitignore` исключает виртуальное окружение, настройки PyCharm, кэши Python,
локальные секреты, журналы, временные файлы и рабочие выгрузки.
Для выгрузок используется путь `exports/`, для временных файлов — `tmp/`
или `temp/`, для локальных секретов — `secrets/` или файлы `.env`.
Создавать эти каталоги заранее не нужно.

Файл `.env.example` можно хранить в Git как образец настроек, если в нём нет
настоящих секретов. `.gitignore` не перестаёт отслеживать файлы, которые
уже были добавлены в Git.

Перед первым коммитом проверить состояние, выбрать файлы и посмотреть
подготовленные изменения:

```powershell
git status
git add main.py README.md .gitignore
git diff --staged
```

В первый коммит должны попасть только `main.py`, `README.md` и `.gitignore`.
После проверки создать коммит:

```powershell
git commit -m "chore: initialize project workspace"
```
