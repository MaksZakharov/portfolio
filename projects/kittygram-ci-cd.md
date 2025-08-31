---
layout: page
title: kittygram-ci-cd
permalink: /projects/kittygram-ci-cd/
---

![Blogicum]({{ '/assets/img/CI CD for Kittygram.png' | relative_url }})

## Описание

**Kittygram** — социальная сеть для обмена фотографиями любимых котиков.  
Проект развёрнут в контейнерах Docker и поддерживает полный цикл CI/CD для автоматического тестирования и деплоя.

## Что сделал

- Создал backend на **Django** с REST API для котиков и пользователей  
- Подключил базу данных **PostgreSQL** в контейнере Docker  
- Настроил работу со статикой и медиа через **Nginx**  
- Настроил Gunicorn для продакшн-развёртывания  
- Реализовал CI/CD через **GitHub Actions**: тесты, линтер, автодеплой на сервер  
- Настроил публикацию образов в **Docker Hub**  
- Подготовил `docker-compose` для развёртывания проекта в контейнерах  

## Технологии

- **Python 3.10**  
- **Django 3.2**  
- **Django REST Framework**  
- **PostgreSQL**  
- **Docker, Docker Compose**  
- **Gunicorn + Nginx**  
- **GitHub Actions (CI/CD)**  

---

## 🔧 Возможности

- ✅ REST API для работы с питомцами  
- ✅ Регистрация и аутентификация пользователей (JWT)  
- ✅ Загрузка фото и управление профилем котика  
- ✅ Хранение данных в PostgreSQL  
- ✅ Полностью контейнеризированный проект  
- ✅ Автоматический деплой на сервер при пуше в `main`  

---

## 🚀 Установка и запуск

Клонируй проект:

```bash
git clone https://github.com/MaksZakharov/kittygram_final.git
cd kittygram_final
```

Создай файл `.env` с переменными окружения:

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

Запусти контейнеры:

```bash
docker compose up -d --build
```

Выполни миграции и собери статику:

```bash
docker compose exec backend python manage.py migrate
docker compose exec backend python manage.py collectstatic --noinput
```

Создай суперпользователя:

```bash
docker compose exec backend python manage.py createsuperuser
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

- Добавить уведомления пользователям  
- Подключить мониторинг контейнеров  
- Добавить систему логирования и алертов  

---

## 📜 Лицензия

Проект создан в рамках учебного курса. Можно использовать в образовательных целях.

---

## Репозиторий на GitHub

[![Перейти к проекту на GitHub](https://img.shields.io/badge/Открыть_проект_на_GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaksZakharov/kittygram_final)
