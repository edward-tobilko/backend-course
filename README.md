# 📘 Backend Course – Express REST API

Навчальний проєкт на **Node.js + Express + TypeScript**, який демонструє, як побудувати REST API з CRUD-операціями.  
Ідеально підходить як стартова база для власних бекенд-проєктів.

---

## 📦 Встановлення та запуск
```bash
git clone https://github.com/edward-tobilko/backend-course.git
cd backend-course
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
- GET /courses – отримати всі курси (фільтрація за ?name=)
- GET /courses/:id – отримати курс за ID
- POST /courses – створити новий курс ({ "name": "front-end" })
- PUT /courses/:id – повне оновлення курсу
- PATCH /courses/:id – часткове оновлення курсу (поле name)
- DELETE /courses/:id – видалити курс

### 📂 Структура проєкту
```typescript
backend_course/
 ├── server.ts          # Головний файл сервера
 ├── package.json       # Скрипти та залежності
 ├── tsconfig.json      # Конфіг TypeScript
 ├── yarn.lock          # Версії залежностей
 ├── dist/              # Зібрані файли (після build)
 └── node_modules/      # Залежності
```

### ⚙️ Технології
- express@5.1.0 – веб-фреймворк
- typescript@5.9.2 – типізація
- nodemon + tsx – гарячий перезапуск у dev
- rimraf – очищення dist перед збіркою

### 📖 Примітки
- Код написаний у стилі модульного API з CRUD.
- Використовується статична in-memory база (dataBase), замість справжньої БД.
- Можна легко адаптувати під PostgreSQL/MongoDB.

### 📖 Автор
eduard.tobilko
#### 🔗 [GitHub] - https://github.com/edward-tobilko
