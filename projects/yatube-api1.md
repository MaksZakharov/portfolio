---
layout: page
title: Yatube API
permalink: /projects/yatube-api/
---

![Yatube API]({{ '/assets/img/yatube_api.png' | relative_url }})

## Описание

REST API для социальной сети **Yatube**, разработанный на **Django REST Framework**.  
Позволяет пользователям публиковать записи, комментировать, подписываться друг на друга и объединяться в группы.  
Реализована аутентификация через **JWT-токены**.

## Что сделал

- Настроил Django REST Framework и подключил JWT-аутентификацию  
- Реализовал эндпоинты для работы с постами, комментариями, группами и подписками  
- Ограничил доступ к изменению и удалению объектов только для авторов  
- Добавил пагинацию, фильтрацию и поиск  
- Подключил документацию **Redoc** и **Swagger**  
- Настроил проект под PEP8 и добавил конфигурации линтеров  
- Подготовил `requirements.txt` для установки зависимостей  

## Технологии

- **Python 3.10**  
- **Django 3.2**  
- **Django REST Framework**  
- **Simple JWT** (аутентификация)  
- **SQLite / PostgreSQL** (база данных)  

---

## 🔧 Возможности

- ✅ Получение списка постов и отдельных публикаций  
- ✅ Создание, редактирование и удаление постов (для авторизованных пользователей)  
- ✅ Работа с комментариями к постам  
- ✅ Подписки на авторов  
- ✅ Доступ к информации о группах  
- ✅ JWT-аутентификация  

---

## 🚀 Установка

Клонируй проект:

```bash
git clone https://github.com/MaksZakharov/api-final-yatube.git
cd api-final-yatube
```

Создай виртуальное окружение (рекомендуется):

```bash
python -m venv venv
source venv/bin/activate       # Linux/macOS
venv\Scripts\activate        # Windows
```

Установи зависимости:

```bash
pip install -r requirements.txt
```

Выполни миграции:

```bash
python manage.py migrate
```

---

## ▶️ Запуск

Запусти сервер разработки:

```bash
python manage.py runserver
```

Документация API будет доступна по адресам:

- Swagger: `http://127.0.0.1:8000/swagger/`  
- Redoc: `http://127.0.0.1:8000/redoc/`  

---

## 📁 Структура проекта

```
api-final-yatube/
├── api/                 # Логика API (сериализаторы, вьюхи, роуты)
├── posts/               # Приложение для работы с постами и группами
├── users/               # Работа с пользователями и подписками
├── yatube_api/          # Настройки проекта
├── manage.py            # Точка входа
├── requirements.txt     # Зависимости
└── README.md            # Документация
```

---

## 🧪 Примеры запросов

### Получение постов
`GET /api/v1/posts/`

### Создание поста
`POST /api/v1/posts/`
```json
{
  "text": "Новая публикация через API",
  "group": 1
}
```

### Получение комментариев
`GET /api/v1/posts/{post_id}/comments/`

### Подписка
`POST /api/v1/follow/`
```json
{
  "following": "username"
}
```

### Авторизация
`POST /api/v1/jwt/create/`
```json
{
  "username": "user",
  "password": "password"
}
```

---

## 🛠 Планы на доработку

- Подключить CI/CD через GitHub Actions  
- Добавить систему уведомлений  
- Вынести проект в Docker  
- Реализовать версионность API  

---

## 📜 Лицензия

Проект создан в рамках учебного курса. Можно использовать в образовательных целях.

---

## Репозиторий на GitHub

[![Перейти к проекту на GitHub](https://img.shields.io/badge/Открыть_проект_на_GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaksZakharov/api-final-yatube)
