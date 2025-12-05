# StudyFlow REST API - Краткая справка

## Основные endpoint'ы

### Аутентификация
```
POST   /auth/register     - Регистрация
POST   /auth/login        - Вход
POST   /auth/logout       - Выход
POST   /auth/refresh      - Обновить токен
```

### Предметы
```
GET    /subjects          - Список всех предметов
GET    /subjects/:id      - Получить предмет
POST   /subjects          - Создать предмет
PUT    /subjects/:id      - Обновить предмет
DELETE /subjects/:id      - Удалить предмет
```

### Задачи
```
GET    /tasks             - Список задач (с фильтрами)
GET    /tasks/:id         - Получить задачу
POST   /tasks             - Создать задачу
PATCH  /tasks/:id         - Частично обновить задачу
DELETE /tasks/:id         - Удалить задачу
```

### Расписание
```
GET    /schedule                  - Расписание на неделю
POST   /schedule/generate         - Сгенерировать с помощью AI
```

### Дедлайны
```
GET    /deadlines         - Список дедлайнов
POST   /deadlines         - Создать дедлайн
PUT    /deadlines/:id     - Обновить дедлайн
DELETE /deadlines/:id     - Удалить дедлайн
```

### Аналитика
```
GET    /analytics/overview            - Общая статистика
GET    /analytics/time-distribution   - Распределение времени
GET    /analytics/productivity        - График продуктивности
```

### Уведомления
```
GET    /notifications             - Список уведомлений
PATCH  /notifications/:id/read    - Отметить прочитанным
POST   /notifications/settings    - Настройки уведомлений
```

### Пользователь
```
GET    /user/profile       - Профиль
PUT    /user/profile       - Обновить профиль
GET    /user/preferences   - Настройки
PUT    /user/preferences   - Обновить настройки
```

## Сценарии использования

### 1. Создание учебного плана
```
1. POST /auth/register           → Регистрация
2. POST /subjects                → Создать предметы
3. POST /schedule/generate       → Сгенерировать расписание
4. GET /schedule                 → Получить расписание
```

### 2. Ежедневная работа
```
1. POST /auth/login              → Войти
2. GET /tasks?date=today         → Задачи на сегодня
3. PATCH /tasks/:id              → Отметить выполненной
4. GET /notifications            → Проверить уведомления
```

### 3. Добавление дедлайна
```
1. POST /deadlines               → Создать дедлайн
2. GET /deadlines?upcoming=true  → Просмотреть предстоящие
3. GET /tasks                    → AI добавит задачи для подготовки
```

### 4. Просмотр статистики
```
1. GET /analytics/overview          → Общая статистика
2. GET /analytics/time-distribution → По предметам
3. GET /analytics/productivity      
→ График продуктивности
```
