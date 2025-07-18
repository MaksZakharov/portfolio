---
layout: page
title: Fridge App
permalink: /projects/fridge/
---

![Fridge App]({{ '/assets/img/fridge.png' | relative_url }})

## Описание

Приложение на Python для учёта продуктов и определения просроченных товаров. Поддерживает добавление вручную и из текстовой заметки.

## Что сделал

- Реализовал функции добавления продуктов вручную и через текстовую заметку (`add`, `add_by_note`)  
- Написал поиск по названию (`find`) и подсчёт общего количества товара (`get_amount`)  
- Реализовал определение просроченных товаров с учётом срока годности (`get_expired`)  
- Обработал ввод и преобразование дат (`datetime.date`) и количеств (`decimal.Decimal`)  
- Оформил код с использованием docstring-комментариев, добавил пример использования в `main`
- Настроил структуру проекта как **пакет** (`fridge/`) с отдельным `run.py` для запуска  
- Подготовил `requirements.txt` и добавил автотесты на ключевые функции (`pytest`)

## Технологии

Python 3, стандартные библиотеки: `datetime`, `decimal`

## 🔧 Возможности

- ✅ Добавление продукта вручную  
- ✅ Добавление продукта по текстовой заметке (в свободной форме)  
- ✅ Поиск по части названия (без учёта регистра)  
- ✅ Подсчёт общего количества продукта  
- ✅ Определение просроченных товаров (с учётом ближайших дней)  
- ✅ Демонстрационный сценарий запуска  
- ⚙️ Поддержка партий одного и того же продукта с разными сроками

---

## 🚀 Установка

Клонируй проект:

```bash
git clone https://github.com/your-username/fridge-app.git
cd fridge-app
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

---

## ▶️ Запуск

Программа запускается через файл `run.py`, который вызывает демонстрационный сценарий:

```bash
python run.py
```

Пример вывода:

```
Поиск 'яйца': ['Яйца']
Сколько воды: 1.5 кг
Просроченные:
- Яйца: 10 кг
- Морковь: 2 кг

Содержимое холодильника:
Яйца:
  - 10 кг, срок: 2023-12-10
Морковь:
  - 2 кг, срок: 2023-12-05
Вода:
  - 1.5 кг, срок: None
```

---

## 📁 Структура проекта

```
fridge-app/
├── fridge/
│   ├── core.py         # Логика добавления, поиска, подсчёта, просрочки
│   ├── main.py         # Демонстрационный запуск (main())
│   ├── utils.py        # Парсинг текстовых заметок
│   └── __init__.py
├── run.py              # Точка входа: запускает main()
├── tests/              # Тесты (по желанию)
│   ├── test_core.py
│   └── __init__.py
├── requirements.txt    # Зависимости (включает pytest)
```

---

## 🧪 Тестирование

Если ты используешь `pytest`, запусти тесты так:

```bash
pytest
```

Примеры тестов покрывают:
- добавление и подсчёт количества продукта
- добавление из текстовой заметки
- определение просроченных продуктов

---

## 🛠 Планы на доработку

- Интерактивное CLI-меню
- Сохранение/загрузка содержимого из файла (например, JSON)
- Поддержка единиц измерения (кг/шт)
- Работа с argparse и аргументами командной строки
- Веб или GUI-интерфейс (Tkinter, PyQt)

---

## 📜 Лицензия

Проект создан в рамках обучения. Можно использовать в образовательных целях.

## Репозиторий на GitHub

[![Перейти к проекту на GitHub](https://img.shields.io/badge/Открыть_проект_на_GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaksZakharov/fridge-app)
