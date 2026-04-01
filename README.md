# Документация VK WorkSpace (демо-проект)

Демонстрационный проект для позиции **технического писателя**.  
Показывает реальное применение подхода **Docs as Code**.

- 🌐 **Сайт документации:**  
  https://annamoskvina-developer.github.io/my-docs/

- 📂 **Исходный код:**  
  https://github.com/AnnaMoskvina-developer/my-docs

---

## 🛠 Используемые технологии

| Инструмент | Назначение |
|------------|------------|
| Markdown | Написание документации |
| Git / GitHub | Контроль версий, CI/CD, хостинг |
| MkDocs + Material | Генератор статического сайта и тема |
| Mermaid | Текстовые диаграммы (архитектура, flowchart, sequence) |
| GitHub Actions | Автоматическая сборка и деплой |
| GitHub Pages | Публикация готового сайта |

---

## 📊 Диаграммы

В проекте используются **Mermaid** — текстовый формат диаграмм, который позволяет хранить схемы в Git вместе с документацией.

| Тип | Описание | Ссылка |
|-----|----------|--------|
| **Архитектура** | Взаимодействие пользователя с сервисами | [посмотреть](https://annamoskvina-developer.github.io/my-docs/advanced-example/#architecture) |
| **Flowchart** | Процесс авторизации | [посмотреть](https://annamoskvina-developer.github.io/my-docs/advanced-example/#flowchart) |
| **Sequence diagram** | Отправка сообщения | [посмотреть](https://annamoskvina-developer.github.io/my-docs/advanced-example/#sequence) |
| **C4 Context** | Контекстная диаграмма системы | [посмотреть](https://annamoskvina-developer.github.io/my-docs/advanced-example/#c4-context-системный-контекст) |

---

## 🚀 Локальный запуск

```bash
git clone https://github.com/AnnaMoskvina-developer/my-docs.git
cd my-docs
pip install mkdocs-material
mkdocs serve
```
После этого откройте браузер и перейдите по адресу:
http://127.0.0.1:8000