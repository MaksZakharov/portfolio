---
layout: page
title: bot-assistant
permalink: /projects/bot-assistant/
---

![Blogicum]({{ '/assets/img/bot-assistant.png' | relative_url }})

## Описание

**Бот-ассистент** — учебный проект Яндекс Практикума.  
Телеграм-бот, который регулярно обращается к API Практикум.Домашка и сообщает пользователю статус проверки домашнего задания.  
Проект демонстрирует работу с API, обработку ошибок, логирование и тестирование с помощью **unittest**.

## Что сделал

- Реализовал телеграм-бота на основе `python-telegram-bot`  
- Настроил запросы к API Практикум.Домашка и обработку ответов  
- Добавил систему логирования с уровнями INFO и ERROR  
- Написал модульные тесты с использованием `unittest`  
- Настроил работу с переменными окружения через `.env`  
- Подготовил структуру проекта и файл зависимостей `requirements.txt`

## Технологии

- **Python 3**  
- **python-telegram-bot** (работа с Telegram API)  
- **Requests** (HTTP-запросы)  
- **python-dotenv** (переменные окружения)  
- **unittest** (автотесты)  
- **Logging** (логирование)  

---

## 🔧 Возможности

- ✅ Получение статуса домашних заданий из API Практикум.Домашка  
- ✅ Уведомления в Telegram о проверке работы  
- ✅ Система логирования (INFO, ERROR)  
- ✅ Проверка переменных окружения  
- ✅ Автотесты (unittest)  

---

## 🚀 Установка

Клонируй проект:

```bash
git clone https://github.com/MaksZakharov/homework-bot.git
cd homework-bot
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

Создай файл `.env` и добавь туда токены:

```env
PRACTICUM_TOKEN=ваш_токен_практикума
TELEGRAM_TOKEN=токен_бота
TELEGRAM_CHAT_ID=ваш_chat_id
```

---

## ▶️ Запуск

Запусти бота:

```bash
python -m homework.main
```

---

## 📁 Структура проекта

```
homework-bot/
├── homework/               # Основной код бота
│   ├── exceptions.py       # Пользовательские исключения
│   ├── settings.py         # Настройки и константы
│   ├── utils.py            # Вспомогательные функции
│   └── main.py             # Точка входа
├── tests/                  # Модульные тесты (unittest)
│   └── test_utils.py
├── requirements.txt        # Зависимости
├── .env.example            # Пример .env файла
└── README.md               # Документация
```

---

## 🧪 Тестирование

Запуск тестов:

```bash
python -m unittest discover tests
```

Тесты проверяют:
- корректность формирования сообщений о статусах  
- обработку исключений  
- работу функций `check_tokens`, `parse_status`, `send_message`  

---

## 🛠 Планы на доработку

- Добавить CI/CD (GitHub Actions) для автотестов  
- Подключить систему логирования в отдельный файл  
- Реализовать обработку нестандартных ошибок API  
- Добавить расширенные уведомления (например, по email)  

---

## 📜 Лицензия

Проект создан в рамках обучения. Можно использовать в образовательных целях.

---

## Репозиторий на GitHub

[![Перейти к проекту на GitHub](https://img.shields.io/badge/Открыть_проект_на_GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaksZakharov/homework-bot)
