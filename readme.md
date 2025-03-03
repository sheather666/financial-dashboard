
# Личный Финансовый Дашборд

## Описание проекта
Проект представляет собой интерактивный дашборд для анализа личных финансов.  
Цель проекта — создание удобного инструмента для анализа доходов, расходов и сбережений.  

Дашборд позволяет:
- Анализировать доходы и расходы с использованием интерактивных фильтров.
- Визуализировать тренды расходов по категориям, времени и пользователям.
- Просматривать данные пользователей, их транзакции и общую финансовую сводку.

## Используемые инструменты
Для реализации проекта использованы следующие инструменты:
- **DuckDB**: Локальная база данных для хранения и обработки данных.
- **Pandas**: Библиотека для обработки и анализа данных.
- **Plotly**: Библиотека для создания интерактивных графиков и диаграмм.
- **Streamlit**: Платформа для создания и визуализации дашборда.

## Структура репозитория
Проект структурирован следующим образом:
- **`source/`**: Исходные данные в формате CSV:
  - `users.csv`: Данные пользователей.
  - `categories.csv`: Категории расходов.
  - `transactions.csv`: Данные о транзакциях.
- **`queries/`**: SQL-скрипты:
  - `create_tables.sql`: Скрипт для создания таблиц.
  - `insert_data.sql`: Скрипт для загрузки данных.
  - `views.sql`: Скрипт для создания вьюшек.
- **`ddl.py`**: Модуль для создания таблиц в базе данных и их заполнения данными.
- **`etl.py`**: Модуль для извлечения данных из базы данных для работы с дашбордом.
- **`main.py`**: Основной модуль для создания интерактивного дашборда.
- **`requirements.txt`**: Список используемых библиотек и их версий.
- **`my.db`**: Файл локальной базы данных DuckDB.

## Как запустить проект
1. Клонируйте репозиторий:
   ```bash
   git clone <URL вашего репозитория>
   cd <название папки репозитория>
   ```
2. Установите необходимые зависимости:
   ```bash
   pip install -r requirements.txt
   ```
3. Убедитесь, что все исходные данные находятся в папке `source/` и файлы `.csv` корректно структурированы.
4. Запустите дашборд:
   ```bash
   streamlit run main.py
   ```
5. Перейдите по адресу [http://localhost:8501](http://localhost:8501), чтобы открыть дашборд.

## Основной функционал
- **Фильтры**:
  - Фильтрация транзакций по пользователям, категориям и типу (доход/расход).
  - Фильтрация по диапазону дат.
- **Диаграммы и графики**:
  - Расходы и доходы по категориям.
  - Тренды расходов по времени (дни недели, месяцы, кварталы).
  - Расходы пользователей с высокой активностью.
- **Статистика пользователей**:
  - Общий доход, расходы и сбережения.
  - Количество транзакций и их распределение.

## Примеры использования SQL
В проекте применены следующие SQL-конструкции:
- **Агрегирующие функции**: Сумма, среднее значение, минимум, максимум.
- **Работа с датами**: Извлечение месяца, года, дня недели из даты транзакции.
- **Оконные функции**: Подсчёт кумулятивной суммы расходов.
- **Подзапросы**: Формирование сложных выборок из таблиц и вьюшек.
- **Джойны**: Объединение данных из разных таблиц.

## Задеплоенный дашборд и репозиторий
- **Дашборд**: [Ссылка на дашборд](https://financial-dashboard-hqghsu2jw6gz9hohzaq2eu.streamlit.app/).
- **Репозиторий**: [Ссылка на GitHub](https://github.com/sheather666/Financial-Dashboard).

## Автор(ы)
- *Абдуллаев С. Ш.*
