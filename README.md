# Документация VK WorkSpace (демо-проект)

Демонстрационный проект для позиции **технического писателя**.  
Показывает реальное применение подхода **Docs as Code**.

- 🌐 **Сайт документации:**  
  [annamoskvina-developer.github.io/my-docs](https://annamoskvina-developer.github.io/my-docs/)

- 📂 **Исходный код:**  
  [github.com/AnnaMoskvina-developer/my-docs](https://github.com/AnnaMoskvina-developer/my-docs)

---

## 🛠 Стек

| Инструмент | Назначение |
|------------|------------|
| Markdown | Написание документации |
| Git / GitHub | Контроль версий, CI/CD, хостинг |
| MkDocs + Material | Генератор статического сайта и тема |
| GitHub Actions | Автоматическая сборка и деплой |
| GitHub Pages | Публикация готового сайта |

---

## 🚀 Локальный запуск

```bash
git clone https://github.com/AnnaMoskvina-developer/my-docs.git
cd my-docs
pip install mkdocs-material
mkdocs serve
Открыть http://127.0.0.1:8000