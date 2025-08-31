---
layout: page
title: kittygram-deploy
permalink: /projects/kittygram-deploy/
---

![Blogicum]({{ '/assets/img/Kittygram.png' | relative_url }})

## Описание

**Kittygram** — это социальная сеть для обмена фотографиями любимых питомцев.  
Пользователи могут публиковать карточки котиков, указывать их достижения, просматривать профили других участников и делиться впечатлениями.

## Что сделал

- Создал backend на **Django** с использованием REST API  
- Настроил аутентификацию и регистрацию пользователей через **Djoser** и JWT  
- Реализовал модели для котиков, пользователей и достижений  
- Организовал работу с изображениями через **Pillow**  
- Настроил деплой проекта на удалённый сервер с использованием **Docker Compose**  
- Подключил **Nginx** и **Gunicorn** для стабильной работы проекта  
- Настроил CI/CD через **GitHub Actions**  

## Технологии

- **Python 3.10**  
- **Django 3.2**  
- **Django REST Framework**  
- **Djoser** (аутентификация)  
- **Pillow** (работа с изображениями)  
- **PostgreSQL**  
- **Docker, Docker Compose**  
- **Gunicorn + Nginx**  
- **GitHub Actions (CI/CD)**  

---

## 🔧 Возможности

- ✅ Регистрация и аутентификация пользователей  
- ✅ Создание и редактирование профилей  
- ✅ Добавление карточек питомцев с фото  
- ✅ Указание достижений питомцев  
- ✅ Просмотр ленты других пользователей  
- ✅ CI/CD деплой проекта на сервер  

---

## 🚀 Установка

Клонируй проект:

```bash
git clone https://github.com/MaksZakharov/kittygram_final.git
cd kittygram_final
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

Создай файл `.env` и укажи в нём переменные окружения:

```
SECRET_KEY=секретный_ключ
DEBUG=False
ALLOWED_HOSTS=127.0.0.1,localhost,<ваш_сервер>
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
DB_HOST=db
DB_PORT=5432
```

Выполни миграции:

```bash
python manage.py migrate
```

---

## ▶️ Запуск

Локальный запуск:

```bash
python manage.py runserver
```

Запуск в Docker:

```bash
docker compose up -d --build
docker compose exec backend python manage.py migrate
docker compose exec backend python manage.py collectstatic --noinput
```

---

## 📁 Структура проекта

```
kittygram_final/
├── backend/             # Backend Django
├── frontend/            # Frontend
├── infra/               # Docker-compose и конфиги
├── nginx/               # Конфигурация Nginx
├── requirements.txt     # Зависимости
├── .env.example         # Пример env-файла
└── README.md            # Документация
```

---

## 🛠 Планы на доработку

- Добавить лайки и комментарии для питомцев  
- Добавить возможность делиться питомцами в соцсетях  
- Реализовать уведомления пользователям  

---

## 📜 Лицензия

Проект создан в рамках учебного курса. Можно использовать в образовательных целях.

---

## Репозиторий на GitHub

[![Перейти к проекту на GitHub](https://img.shields.io/badge/Открыть_проект_на_GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaksZakharov/infra_sprint1)
