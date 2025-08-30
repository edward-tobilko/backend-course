# Backend Course – Express + TypeScript Setup

## 🚀 Запуск у режимі розробки - yarn dev:

Використовується nodemon + tsx.
Автоматичний рестарт при зміні .ts файлів.
TypeScript виконується напряму без збірки у dist/.

## 🐞 Запуск з дебагером - yarn debug:

Запускає сервер з --inspect (порт 9229).
Можна підключати Chrome DevTools (chrome://inspect) або VS Code.
Breakpoints працюють напряму у .ts.

## 📦 Продакшн-режим - yarn build and yarn start:

**build** - компілює TypeScript у dist/.
**start** - запускає готовий JS через Node.
Використовується тільки у продакшн, без nodemon і без дебага.

## 🛠 Структура:

```typescript
backend_course/
 ├── server/        # вихідні .ts файли (точка входу: server.ts)
 ├── src/           # додаткові модулі/сторінки
 ├── dist/          # згенерований JS (створюється після build)
 ├── package.json   # скрипти та залежності
 └── tsconfig.json  # налаштування TypeScript

```

- **rimraf** - видаля старий dist та пушить відразу новий, за доп. yarn build.
