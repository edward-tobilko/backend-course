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
yarn debug:build
```

### Збірка та продакшн
```bash
yarn build
yarn start
```

#### Сервер запускається за замовчуванням на http://localhost:3007/courses.

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
src/
 ├── __tests__/               # E2E та юніт-тести
 │   └── courses.e2e.test.ts
 │
 ├── config/                  # Налаштування середовища
 │   └── env.ts
 │
 ├── controllers/             # Контролери (приймають HTTP-запити)
 │   └── courses.controller.ts
 │
 ├── db/                      # In-memory база або підключення до БД
 │   └── courses.db.ts
 │
 ├── middlewares/             # Middleware (валидація, логування, помилки)
 │   └── courses.middleware.ts
 │
 ├── repositories/            # Репозиторії (робота з даними)
 │   └── courses.repo.ts
 │
 ├── routes/                  # Роутери (шляхи API)
 │   └── courses.route.ts
 │
 ├── services/                # Бізнес-логіка
 │   └── courses.service.ts
 │
 ├── types/                   # Типи TypeScript
 │   ├── course.types.ts
 │   └── index.d.ts
 │
 ├── utils/                   # Утиліти
 │   ├── http-codes.ts
 │   ├── logger.ts
 │   └── normalize.ts
 │
 ├── validators/              # Валідація даних
 │   └── courses.schema.ts
 │
 ├── app.ts                   # Ініціалізація застосунку Express
 └── server.ts                # Точка входу (start server)

theory/                       # Навчальні матеріали/чернетки
.env.example                  # Приклад змінних середовища
.gitignore                    # Ігноровані файли
eslint.config.js              # Налаштування ESLint
package.json                  # Залежності та скрипти
tsconfig.json                 # Конфіг TypeScript
tsconfig.build.json           # Конфіг для збірки
yarn.lock                     # Версії залежностей
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
