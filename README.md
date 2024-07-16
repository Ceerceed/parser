# Telegram Bot для Парсинга Вакансий с hh.ru

Этот Telegram-бот предназначен для поиска вакансий на сайте hh.ru с использованием api.hh.ru. Бот позволяет настраивать фильтры, выбирать количество вакансий для отображения, сохранять результаты в базу данных и экспортировать их в чат или CSV-файл.

## Требования

- Docker
- Telegram

## Установка

1. **Скачайте и распакуйте проект:**
   ```bash
   git clone https://github.com/yourusername/hhparser.git
   cd hhparser
   ```

2. **Создайте файл `.env`:**
   ```bash
   touch .env
   ```

3. **Заполните файл `.env` следующим содержимым:**
   ```
   TELEGRAM_BOT_TOKEN=Ваш_Токен
   ```
   Замените `Ваш_Токен` на токен вашего Telegram-бота, который можно получить у BotFather.

4. **Запустите контейнер Docker:**
   ```bash
   docker-compose up --build
   ```

5. **Найдите бота в Telegram и начните с ним взаимодействовать, нажав "Start" или "Запустить".**

## Использование

### Команды

- **/start**
  - Инициализация бота. Используйте эту команду при первом запуске или после долгого перерыва.

- **/search**
  - Запуск поиска вакансий. Пошаговый процесс включает:
    1. Ввод названия вакансии.
    2. Ввод региона (1 = Москва, 2 = Санкт-Петербург и т.д.).
    3. Ввод количества вакансий для отображения.
    4. Настройка фильтров (зарплата, опыт работы, тип занятости, график работы).
    5. Запуск поиска.

### Фильтры

- **Зарплата:** Укажите диапазон в формате "от-до".
- **Опыт работы:** Выберите требуемый уровень опыта.
- **Тип занятости:** Укажите тип занятости.
- **График работы:** Укажите предпочтительный график.
- **Сброс фильтров:** Сбрасывает все выбранные фильтры.

### Сохранение и экспорт

- **/save**
  - Сохраняет найденные вакансии в базу данных.

- **/export**
  - Экспортирует сохраненные вакансии в CSV-файл или отправляет их в чат.

- **/clear**
  - Очищает базу данных от сохраненных вакансий.

## Лицензия

Этот проект лицензирован под MIT License - подробности в файле LICENSE.

## Контакты

Если у вас есть вопросы или предложения, пожалуйста, свяжитесь с [вашим именем или почтой].

---

Этот README файл помогает понять основные функции бота и содержит все необходимые шаги для его установки и использования.
