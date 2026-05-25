# Codex Skills

Моя коллекция скилов для Codex.  
Они помогают аккуратнее выполнять задачи, улучшать код, готовить проекты к GitHub, делать учебные работы понятными и создавать современный интерфейс.

## Скилы

### `universal-premium-ui-style`

Скилл для современного визуального стиля интерфейсов.

Он нужен, чтобы Codex делал интерфейсы более аккуратными, минималистичными и похожими на готовый продукт, а не на сырой учебный макет.

Подходит для:

- сайтов
- мобильных приложений
- десктопных приложений
- админ-панелей
- dashboard-страниц
- виджетов
- лендингов
- форм
- модальных окон
- AI-чатов
- прототипов

Пример использования:

Use the universal-premium-ui-style skill when creating or redesigning the interface.

---

### `codex-task-executor`

Скилл для безопасного выполнения задач в проекте.

Он нужен, чтобы Codex не начинал сразу переписывать всё подряд, а сначала разобрался в проекте, нашёл нужные файлы и внёс точные изменения.

Что он помогает делать:

- сначала изучать структуру проекта
- находить нужные файлы
- понимать текущую архитектуру
- менять только то, что относится к задаче
- не ломать существующую логику
- проверять результат, если это возможно
- кратко писать, что было изменено

Пример использования:

Use the codex-task-executor skill to complete this task safely and fully.

---

### `github-repo-polisher`

Скилл для подготовки проекта к публикации на GitHub.

Он нужен, чтобы репозиторий выглядел аккуратно и понятно для других людей.

Что он помогает делать:

- улучшать README.md
- добавлять или исправлять .gitignore
- проверять структуру проекта
- убирать лишние файлы
- не выкладывать случайно токены, пароли и .env
- добавлять инструкцию по запуску
- делать проект понятнее для просмотра
- готовить учебные и портфолио-проекты к публикации

Пример использования:

Use the github-repo-polisher skill to prepare this project for publication on GitHub.

---

### `student-homework-builder`

Скилл для учебных заданий и лабораторных работ.

Он нужен, чтобы Codex выполнял задание по требованиям преподавателя, но не делал проект слишком сложным и “нереалистично профессиональным”.

Что он помогает делать:

- внимательно соблюдать требования задания
- не добавлять лишнее без необходимости
- писать понятный код
- делать структуру, которую можно объяснить преподавателю
- добавлять нормальные тестовые данные, если они нужны
- готовить проект к сдаче или защите
- сохранять стиль сильной, но всё ещё учебной работы

Подходит для:

- ASP.NET Core
- Razor Pages / MVC
- Python
- C#
- WinForms / WPF
- SQL
- Microsoft Access
- Android
- HTML / CSS / JavaScript
- небольших учебных приложений

Пример использования:

Use the student-homework-builder skill to keep the solution aligned with the assignment and explainable for a student.

---

## Структура репозитория

codex-skills/
├─ README.md
└─ skills/
   ├─ universal-premium-ui-style/
   │  └─ SKILL.md
   ├─ codex-task-executor/
   │  └─ SKILL.md
   ├─ github-repo-polisher/
   │  └─ SKILL.md
   └─ student-homework-builder/
      └─ SKILL.md

## Установка

Чтобы использовать скилл только в одном проекте, скопируй нужную папку скила сюда:

your-project/
└─ .agents/
   └─ skills/
      ├─ codex-task-executor/
      │  └─ SKILL.md
      └─ universal-premium-ui-style/
         └─ SKILL.md

Путь внутри проекта:

your-project/.agents/skills/

Чтобы использовать скилы во всех проектах, положи их в глобальную папку:

~/.agents/skills/

На Windows это обычно выглядит так:

C:\Users\YOUR_USERNAME\.agents\skills\

Пример:

C:\Users\YOUR_USERNAME\.agents\skills\codex-task-executor\SKILL.md

## Полезные сочетания скилов

### Обычная задача по программированию

Use the codex-task-executor skill to complete this task safely and fully.

### Задача с интерфейсом

Use the codex-task-executor skill to complete this task safely and fully.
If the task includes UI, also use the universal-premium-ui-style skill.

### Учебное задание

Use the codex-task-executor skill to complete the task safely and fully.
Use the student-homework-builder skill to keep the solution aligned with the assignment and explainable for a student.

### Учебное задание с интерфейсом

Use the codex-task-executor skill to complete the task safely and fully.
Use the student-homework-builder skill to keep the solution aligned with the assignment and explainable for a student.
If the task includes UI, also use the universal-premium-ui-style skill.

### Подготовка проекта к GitHub

Use the github-repo-polisher skill to prepare this project for publication on GitHub.
Use the codex-task-executor skill to make changes safely and verify the result.

### Подготовка учебного проекта к GitHub

Use the codex-task-executor skill.
Use the student-homework-builder skill.
Use the github-repo-polisher skill to prepare the repository for GitHub.
If the project includes UI, also use the universal-premium-ui-style skill.

## Примеры использования

Use the codex-task-executor skill to inspect this project and fix the bug.
Do not rewrite unrelated files.
After changes, run the available checks and report what was changed.

Use the student-homework-builder skill to complete this ASP.NET Core Razor Pages assignment.
Keep the solution understandable for a student and do not overengineer it.

Use the github-repo-polisher skill to clean this repository before GitHub publication.
Create or improve README.md, add a proper .gitignore, and check that no secrets are exposed.

Use the universal-premium-ui-style skill to redesign this dashboard.
Keep the interface dark, modern, minimal, responsive, and production-ready.
