# Drone Control System

Система управления беспилотниками с функциями авторизации, регистрации, выбора беспилотника и пультом удаленного управления.

## Функциональность

- Регистрация и авторизация пользователей
- Выбор беспилотника из доступного списка
- Панель управления беспилотником в реальном времени
- Мониторинг параметров беспилотника (заряд батареи, высота, расстояние и т.д.)
- Управление камерой (фото и видеосъемка)

## Технические детали

- Frontend: React, TypeScript, Styled Components
- Routing: React Router
- Аутентификация: Firebase Authentication
- База данных: Firebase Firestore

## Установка и запуск

1. Клонируйте репозиторий:
```bash
git clone <url-репозитория>
cd drone-control-system
```

2. Установите зависимости:
```bash
npm install
```

3. Настройте Firebase:
   - Создайте проект в [Firebase Console](https://console.firebase.google.com/)
   - Включите Authentication и Firestore
   - Скопируйте настройки проекта в файл `src/firebase.ts`

4. Запустите проект в режиме разработки:
```bash
npm start
```

## Настройка Firebase

В файле `src/firebase.ts` замените данные конфигурации на свои:

```typescript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

## Структура проекта

- `src/components` - UI компоненты
- `src/contexts` - React контексты (AuthContext и др.)
- `src/pages` - Основные страницы приложения
- `src/firebase.ts` - Конфигурация Firebase

## Производственная версия

Для создания production-сборки:

```bash
npm run build
```

Файлы сборки будут размещены в директории `build/`.
