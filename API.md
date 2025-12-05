# StudyFlow REST API

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
GET    /subjects/{id}      - Получить предмет
POST   /subjects          - Создать предмет
PUT    /subjects/{id}      - Обновить предмет
DELETE /subjects/{id}      - Удалить предмет
```

### Задачи
```
GET    /tasks             - Список задач (с фильтрами)
GET    /tasks/{id}         - Получить задачу
POST   /tasks             - Создать задачу
PATCH  /tasks/{id}         - Частично обновить задачу
DELETE /tasks/{id}         - Удалить задачу
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
PUT    /deadlines/{id}     - Обновить дедлайн
DELETE /deadlines/{id}     - Удалить дедлайн
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
PATCH  /notifications/{id}/read    - Отметить прочитанным
POST   /notifications/settings    - Настройки уведомлений
```

### Пользователь
```
GET    /user/profile       - Профиль
PUT    /user/profile       - Обновить профиль
GET    /user/preferences   - Настройки
PUT    /user/preferences   - Обновить настройки
```
