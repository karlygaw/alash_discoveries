# Alash Discoveries
Alash Discoveries - это веб-приложение для бронирования туров по Казахстану. Оно позволяет пользователям бронировать и оставлять отзывы и администраторам добавлять, просматривать, обновлять и удалять туры, управлять бронированиями, отзывами и учетными записями пользователей.

## Содержание
- [Технологии](#технологии)
- [Начало работы](#начало-работы)
- [Тестирование](#тестирование)
- [CI/CD](#deploy-и-ci/cd)
- [Contributing](#contributing)
- [To do](#to-do)
- [Команда проекта](#команда-проекта)

## Технологии
- [Node.js](https://nodejs.org/en)
- [Express.js](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/)
- [Mongoose](https://mongoosejs.com/)
- [React](https://react.dev/)

### Требования
Для установки и запуска проекта, необходим [NodeJS](https://nodejs.org/) v8+.

### Установка кода
Склонируйте репозиторий: `git clone https://github.com/karlygaw/alash_discoveries`

### Установка зависимостей
Для установки зависимостей, выполните команду:
```sh
$ cd frontend
```
```sh
$ npm i
```
```sh
$ cd backend
```
```sh
$ npm i
```

### Запуск Development сервера
Чтобы запустить сервер для разработки, выполните команду:
backend:
```sh
/backend
npm run start-dev
```
```sh
/frontend
npm start
```

### Создание билда
Чтобы выполнить production сборку, выполните команду: 
```sh
cd ..
npm run build
```

## Тестирование
Какие инструменты тестирования использованы в проекте и как их запускать. Например:

Наш проект покрыт юнит-тестами Jest. Для их запуска выполните команду:
```sh
npm run test
```

## Использование API
### Авторизация
- POST /api/v1/auth/register - Регистрация нового пользователя
- POST /api/v1/auth/login - Вход пользователя
### Пользователи
- GET /api/v1/users - Получить список всех пользователей (только для администраторов)
- GET /api/v1/users/:id - Получить информацию о пользователе по ID (только для администраторов)
- DELETE /api/v1/users/:id - Удалить пользователя по ID (только для администраторов)
### Туры
- GET /api/v1/tours - Получить список всех туров
- GET /api/v1/tours/:id - Получить информацию о туре по ID
- POST /api/v1/tours - Добавить новый тур (только для администраторов)
- PUT /api/v1/tours/:id - Обновить информацию о туре по ID (только для администраторов)
- DELETE /api/v1/tours/:id - Удалить тур по ID (только для администраторов)
### Бронирования
- GET /api/v1/booking - Получить список всех бронирований (только для администраторов)
- POST /api/v1/booking - Забронировать тур (только для авторизованных пользователей)
- DELETE /api/v1/booking/:id - Удалить бронирование по ID (только для администраторов)
### Отзывы
- GET /api/v1/review - Получить список всех отзывов
- POST /api/v1/review - Добавить новый отзыв (только для авторизованных пользователей)
- DELETE /api/v1/review/:id - Удалить отзыв по ID (только для администраторов)
## Примеры запросов
### Получение списка туров
- Request
- Method: GET
- URL: /api/v1/tours
- Response
- Type: JSON Array
- Fields: name (String), description (String), price (Number), duration (Number), locations (Array of Strings)
### Добавление нового тура
- Request
- Method: POST
- URL: /api/v1/tours
- Body: JSON { name (String, required), description (String), price (Number, required), duration (Number), locations (Array of Strings) }
- Response
- Type: JSON Object
- Fields: message (String)
### Обновление информации о туре
- Request
- Method: PUT
- URL: /api/v1/tours/:id
- Params: id (String, required)
- Body: JSON { name (String), description (String), price (Number), duration (Number), locations (Array of Strings) }
- Response
- Type: JSON Object
- Fields: message (String)
### Удаление тура
- Request
- Method: DELETE
- URL: /api/v1/tours/:id
- Params: id (String, required)
- Response
- Type: JSON Object
-Fields: message (String)

## Contributing
-- Предложения и баг-репорты
Если у вас есть идеи по улучшению проекта или вы столкнулись с какой-то проблемой, пожалуйста, создайте новый issue в разделе Issues нашего репозитория. Обязательно укажите ясное описание проблемы или предложения, а также любую дополнительную информацию, которая может помочь нам понять или воспроизвести проблему.

-- Отправка доработок (Pull Requests)
Если вы хотите внести изменения в проект, создайте новую ветку для своих изменений на основе последней версии main ветки. После завершения своих изменений, откройте Pull Request (PR) в нашем репозитории. Убедитесь, что ваш PR содержит описание ваших изменений и ссылку на связанный issue, если таковой имеется.


### Зачем вы разработали этот проект?
Проект был разработан с целью развития туризма в Казахстане. Мы, авторы проекта, самые любящие путешествовать люди и решили создать этот проект, чтобы сделать путешествия по Казахстану более доступными и удобными для всех.

## To do
- [x] Архитектура и Дизайн Приложения
- [x] Разработка Frontend
- [x] Разработка Backend
- [x] Безопасность и Производительность
- [x] CI/CD
- [x] Качество кода и Документация

## Команда проекта - сткденты 3го курса:

- [Карлыгаш Усен](https://github.com/karlygaw) — Full-stack deleloper
- [Гульназ Омирзакова](https://github.com/oonoky) — Full-stack deleloper

## Credits
Вся заслуга оригинальных идей принадлежит [авторам](https://github.com/karlygaw/alash_discoveries).
