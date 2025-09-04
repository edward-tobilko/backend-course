# 📘 Backend Course – Express REST API

Цей проєкт реалізує простий REST API для управління курсами.  
Він написаний на **Node.js + Express + TypeScript** і включає приклади CRUD-операцій.

---

## 🚀 Запуск проєкту

### Встановлення
```bash
yarn install
```

### Режим розробки
```bash 
yarn dev
```

### Debug-режим
```bash
yarn debug
```

### Збірка та продакшн
```bash
yarn build
```

#### Сервер запускається за замовчуванням на http://localhost:3007.

## 📌 API Маршрути

Courses
GET /courses – отримати всі курси (фільтрація за ?name=)
GET /courses/:id – отримати курс за ID
POST /courses – створити новий курс ({ "name": "front-end" })
PUT /courses/:id – повне оновлення курсу
PATCH /courses/:id – часткове оновлення курсу (поле name)
DELETE /courses/:id – видалити курс
