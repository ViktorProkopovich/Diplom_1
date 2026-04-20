# 🍔 Проект Diplom_Part2 — Юнит-тесты для *Stellar Burgers*

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Pytest-Unit_Tests-orange?logo=pytest" alt="Pytest">
  <img src="https://img.shields.io/badge/Coverage-100%25-brightgreen?logo=codecov" alt="Coverage">
  <img src="https://img.shields.io/badge/Mock-UnitTest-yellow?logo=python" alt="Mock">
</p>

---

## 📘 Описание проекта

В проекте написаны **юнит-тесты для класса `Burger`** учебного приложения космической бургерной **Stellar Burgers**.  
Проверяются ключевые сценарии работы с бургерами: инициализация, добавление/удаление ингредиентов, расчёт стоимости и формирование описания.

---

## 🧪 Тестовые сценарии

### 👤 Класс `Burger` — Инициализация
- Успешное создание бургера с валидным списком ингредиентов.  
- Обработка `None` в списке ингредиентов.  
- Обработка пустого списка ингредиентов.  

---

### 🥬 Работа с ингредиентами
- Добавление валидного ингредиента через `add_ingredient()`.  
- Попытка добавить `None` вместо ингредиента.  
- Удаление существующего ингредиента через `remove_ingredient()`.  
- Попытка удалить несуществующий ингредиент.  

---

### 💰 Расчёт стоимости и описание
- Расчёт общей стоимости бургера с ингредиентами через `get_price()`.  
- Расчёт стоимости без ингредиентов.  
- Обработка `None` в цене ингредиента.  
- Формирование строки-описания бургера через `get_description()`.  
- Обработка `None` в названии ингредиента.  

---

## 📁 Структура проекта

~~~text
Diplom_1_QA_Python_YaPracticum/
│
├── src/                          # Исходный код приложения
│   └── burger.py                 # Класс Burger для тестирования
│
├── tests/                        # Юнит-тесты Pytest
│   ├── test_burger_init.py       # Тесты конструктора __init__
│   ├── test_burger_add.py        # Тесты add_ingredient()
│   ├── test_burger_remove.py     # Тесты remove_ingredient()
│   ├── test_burger_price.py      # Тесты get_price()
│   └── test_burger_description.py # Тесты get_description()
│
├── data/                         # Тестовые данные
│   └── constants.py              # Константы и фикстуры
│
├── conftest.py                   # Фикстуры Pytest (подготовка данных)
├── .gitignore                    # Исключаемые файлы/папки
├── README.md                     # Описание проекта
└── requirements.txt              # Зависимости
~~~

---

## ⚙️ Запуск тестов

### 1️⃣ Клонировать репозиторий

~~~bash
git clone https://github.com/ViktorProkopovich/Diplom_1_QA_Python_YaPracticum.git
cd Diplom_1_QA_Python_YaPracticum
~~~

---

### 2️⃣ Создать и активировать виртуальное окружение

~~~bash
python -m venv venv
~~~

**Активация:**

🪟 **Windows**  
~~~bash
venv\Scripts\activate
~~~

🐧 **MacOS / Linux**  
~~~bash
source venv/bin/activate
~~~

---

### 3️⃣ Установить зависимости

~~~bash
pip install -r requirements.txt
~~~

---

### 4️⃣ Запустить тесты

~~~bash
pytest -v --cov=src --cov-report=term
~~~

---

### 5️⃣ Просмотреть отчёт о покрытии

~~~bash
# HTML-отчёт
pytest -v --cov=src --cov-report=html

# Открыть в браузере
start htmlcov/index.html          # Windows
open htmlcov/index.html           # MacOS
xdg-open htmlcov/index.html       # Linux
~~~

---

## 🧠 Что покрывают тесты

| Категория | Проверки |
|------------|-----------|
| **Конструктор `__init__`** | Валидные данные, `None`, пустой список, параметризация |
| **`add_ingredient()`** | Добавление валидного ингредиента, обработка `None` |
| **`remove_ingredient()`** | Удаление существующего/несуществующего ингредиента, моки |
| **`get_price()`** | Расчёт суммы, обработка `None` в цене ингредиента |
| **`get_description()`** | Формирование описания, обработка `None` в названии |

---

## 🧩 Используемые технологии

- 🐍 **Python 3.10+**  
- 🧪 **Pytest** — фреймворк для тестирования  
- 🎭 **unittest.mock** — мокирование зависимостей  
- 🔁 **@pytest.mark.parametrize** — параметризация тестов  
- 📊 **pytest-cov** — измерение покрытия кода (100%)  
- ⚙️ **Фикстуры** — подготовка и очистка тестовых данных  

---

## 👨‍💻 Автор

**Виктор Прокопович**  
🎓 Студент курса *«Инженер по тестированию: от новичка до автоматизатора»* — **Яндекс Практикум**  
📦 GitHub — [ViktorProkopovich](https://github.com/ViktorProkopovich)
