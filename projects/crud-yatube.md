---
layout: page
title: crud-yatube
permalink: /projects/crud-yatube/
---

![Blogicum]({{ '/assets/img/CRUD for Yatube.png' | relative_url }})

## Описание

**CRUD для Yatube** — учебный проект социальной сети из курса Яндекс Практикума.  
Проект реализует базовый функционал: создание, чтение, обновление и удаление постов, комментариев и групп.  
Основная цель — закрепить навыки работы с Django и Django REST Framework.

## Что сделал

- Настроил Django-проект и подключил базу данных SQLite  
- Создал модели для постов, комментариев и групп  
- Реализовал сериализаторы и CRUD-представления с помощью Django REST Framework  
- Настроил маршруты для работы с API  
- Подключил JWT-аутентификацию для пользователей  
- Подготовил тесты для проверки API  
- Оформил структуру проекта и `requirements.txt`  

## Технологии

- **Python 3**  
- **Django 3.2**  
- **Django REST Framework**  
- **Simple JWT**  
- **SQLite**  
- **Pytest**  

---

## 🔧 Возможности

- ✅ Регистрация и аутентификация пользователей (JWT)  
- ✅ CRUD для постов  
- ✅ CRUD для комментариев  
- ✅ Работа с группами  
- ✅ Подписка на авторов  

---

## 🚀 Установка

Клонируй проект:

```bash
git clone https://github.com/MaksZakharov/api-yatube.git
cd api-yatube
```

Создай виртуальное окружение:

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

Запусти сервер:

```bash
python manage.py runserver
```

---

## 📁 Структура проекта

```
api-yatube/
├── api/                     # Реализация API
├── posts/                   # Приложение постов и комментариев
├── users/                   # Приложение пользователей
├── tests/                   # Тесты
├── manage.py
├── requirements.txt
└── README.md
```

---

## 🧪 Тестирование

Запуск тестов:

```bash
pytest
```

Тесты проверяют:
- корректность работы CRUD для постов и комментариев  
- аутентификацию и права доступа  
- работу сериализаторов и маршрутов  

---

## 🛠 Планы на доработку

- Расширить систему подписок  
- Добавить пагинацию и поиск по постам  
- Подключить CI/CD для автотестов  

---

## 📜 Лицензия

Проект создан в рамках обучения. Можно использовать в образовательных целях.

---

## Репозиторий на GitHub

[![Перейти к проекту на GitHub](https://img.shields.io/badge/Открыть_проект_на_GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaksZakharov/api-yatube)
