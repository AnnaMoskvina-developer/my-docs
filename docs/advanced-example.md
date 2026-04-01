# Продвинутые возможности Markdown

## Сноски {#footnotes}

Техническая документация часто требует пояснений[^1]. Сноски можно добавлять в любом месте[^2].

[^1]: Это пример сноски. Она появляется внизу страницы.
[^2]: Сноски нумеруются автоматически.

---

## Предупреждения и заметки {#admonitions}

!!! note "Примечание"
    Это просто заметка. Дополнительная информация.

!!! warning "Внимание"
    Важная информация, требующая внимания.

!!! danger "Опасно!"
    Действие может привести к потере данных.

---

## Сворачиваемые блоки {#collapsible}

<details>
<summary>Нажмите, чтобы увидеть подробности</summary>

Здесь может быть:
- Любой текст
- Таблицы
- Код

```bash
docker run -d -p 80:80 nginx
```

</details>

---

## Список задач {#tasklist}

- [x] Изучить базовый Markdown
- [x] Создать репозиторий на GitHub
- [x] Настроить MkDocs
- [ ] Добавить продвинутые элементы
- [ ] Опубликовать на GitHub Pages

---

## Сложная таблица {#table}

| Параметр | Тип | Обязательный | Описание | Пример |
|----------|------|--------------|----------|--------|
| `name` | string | ✅ | Имя пользователя | `"Anna"` |
| `age` | integer | ❌ | Возраст | `25` |
| `roles` | array | ❌ | Список ролей | `["admin", "user"]` |

---

## Код с пояснениями {#code}

```python
def process_data(data):
    """Обработка данных"""
    if not data:  # Проверка на пустые данные
        return []
    
    result = [item for item in data if item.is_valid()]
    return result
```

---

## Ссылки на заголовки {#links}

Перейти к [разделу о сносках](#footnotes) или к [таблице](#table).

---

## Изображение {#image}

Вот пример того, как вставлять изображения в документацию:

![Скриншот документации](images/imageforme.png){ width="400" }

*Рисунок 1 — Пример оформления документации (ширина 400px)*

---

## Диаграмма архитектуры {#architecture}

Ниже показана примерная архитектура взаимодействия компонентов в корпоративном сервисе (на основе VK WorkSpace):

```mermaid
graph TD
    A[Пользователь] --> B[Мессенджер]
    A --> C[Почта]
    A --> D[Календарь]
    A --> E[Облачное хранилище]
    
    B --> F[API Gateway]
    C --> F
    D --> F
    E --> F
    
    F --> G[Сервис аутентификации]
    F --> H[Сервис уведомлений]
    F --> I[Сервис документов]
    
    G --> J[База данных пользователей]
    I --> K[Редактор документов]
```

---

## Flowchart (блок-схема процесса) {#flowchart}

Ниже показан процесс авторизации пользователя в системе:

```mermaid
flowchart TD
    A[Пользователь открывает приложение] --> B{Есть активная сессия?}
    B -->|Да| C[Доступ разрешён]
    B -->|Нет| D[Показать форму входа]
    D --> E[Пользователь вводит логин и пароль]
    E --> F{Данные верны?}
    F -->|Да| G[Создать сессию]
    G --> C
    F -->|Нет| H[Показать ошибку]
    H --> D
    C --> I[Работа с системой]
```

---

## Sequence diagram (диаграмма последовательности) {#sequence}

Диаграмма показывает порядок взаимодействия при отправке сообщения в мессенджере:

```mermaid
sequenceDiagram
    participant U as Пользователь
    participant F as Фронтенд
    participant API as API Gateway
    participant A as Auth Service
    participant M as Messenger Service
    participant DB as База данных

    U->>F: Написать сообщение
    F->>API: POST /message
    API->>A: Проверить токен
    A-->>API: Токен валиден
    API->>M: Отправить сообщение
    M->>DB: Сохранить сообщение
    DB-->>M: Подтверждение
    M-->>API: Сообщение доставлено
    API-->>F: Статус 200
    F-->>U: Сообщение отправлено ✓
```

---

## C4 Context (системный контекст):

Контекстная диаграмма показывает, как пользователи взаимодействуют с системой VK WorkSpace и какие внешние системы задействованы.

```mermaid
flowchart TB
    User[<b>👤 Пользователь</b><br/>Сотрудник компании]

    subgraph VKWS [<b>VK WorkSpace</b>]
        direction LR
        Platform[Платформа<br/>корпоративных<br/>коммуникаций]
    end

    subgraph External [<b>Внешние системы</b>]
        Mail[<b>📧 Корпоративная почта</b><br/>Exchange / Gmail]
        Storage[<b>☁️ Файловое хранилище</b><br/>S3 / SharePoint]
    end

    User -->|Использует| Platform
    Platform -->|Отправляет письма| Mail
    Platform -->|Синхронизирует файлы| Storage

    style User fill:#e3f2fd,stroke:#1565c0,stroke-width:2px
    style VKWS fill:#f3e5f5,stroke:#6a1b9a,stroke-width:2px
    style Platform fill:#f3e5f5,stroke:#6a1b9a,stroke-width:2px
    style External fill:#fff8e1,stroke:#ff8f00,stroke-width:2px
    style Mail fill:#fff8e1,stroke:#ff8f00,stroke-width:2px
    style Storage fill:#fff8e1,stroke:#ff8f00,stroke-width:2px
```