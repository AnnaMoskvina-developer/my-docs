# Документация VK WorkSpace (демонстрационный проект)

Демонстрационный проект для позиции **технического писателя**.  
Показывает реальное применение подхода **Docs as Code**.

---

## 📂 Исходный код

Репозиторий с документацией и историей изменений:  
[https://github.com/AnnaMoskvina-developer/my-docs](https://github.com/AnnaMoskvina-developer/my-docs)

---

## 🌐 Готовый сайт

Сайт собран из Markdown с помощью MkDocs и доступен на двух площадках:

| Площадка | Адрес | Назначение |
|----------|-------|------------|
| **GitHub Pages** | [annamoskvina-developer.github.io/my-docs](https://annamoskvina-developer.github.io/my-docs/) | Основной, автоматическая сборка через GitHub Actions |
| **Yandex Cloud** | [annamoskvina-docs.website.yandexcloud.net](https://annamoskvina-docs.website.yandexcloud.net) | Зеркало для стабильного доступа из России |

---

## 🛠 Используемые технологии

| Инструмент | Назначение |
|------------|------------|
| Markdown | Написание документации |
| Git / GitHub | Контроль версий, CI/CD, хостинг кода |
| MkDocs + Material | Генератор статического сайта и тема оформления |
| Mermaid | Текстовые диаграммы (архитектура, flowchart, sequence) |
| GitHub Actions | Автоматическая сборка и публикация на GitHub Pages |
| Yandex Cloud | Зеркало сайта для стабильного доступа из РФ |

---

## 📊 Диаграммы

В проекте используются **Mermaid** — текстовый формат диаграмм, который позволяет хранить схемы в Git вместе с документацией.

| Тип | Описание | Ссылка |
|-----|----------|--------|
| **Архитектура** | Взаимодействие пользователя с сервисами | [посмотреть](https://annamoskvina-developer.github.io/my-docs/advanced-example/#architecture) |
| **Flowchart** | Процесс авторизации | [посмотреть](https://annamoskvina-developer.github.io/my-docs/advanced-example/#flowchart) |
| **Sequence diagram** | Отправка сообщения | [посмотреть](https://annamoskvina-developer.github.io/my-docs/advanced-example/#sequence) |
| **C4 Context** | Контекстная диаграмма системы | [посмотреть](https://annamoskvina-developer.github.io/my-docs/advanced-example/#c4-context-системный-контекст) |

Все диаграммы написаны в формате Mermaid, хранятся в Git и автоматически рендерятся на сайте.

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