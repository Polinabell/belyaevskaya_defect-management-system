# Система управления дефектами на строительных объектах

## Описание проекта

**НАЧАЛЬНАЯ ВЕРСИЯ ПРОЕКТА**

Веб-приложение для управления дефектами на строительных объектах.
На данный момент реализована базовая архитектура и основные компоненты системы.

## Быстрый старт

### Требования
- Docker и Docker Compose
- Python 3.11+
- Node.js 18+

### Запуск в разработке

1. Клонируйте репозиторий:
```bash
git clone <repository-url>
cd belyaevskaya_defect-management-system
```

2. Запустите через Docker Compose:
```bash
docker-compose up --build
```

3. Выполните миграции:
```bash
docker-compose exec backend python manage.py migrate
```

4. Создайте суперпользователя:
```bash
docker-compose exec backend python manage.py createsuperuser
```

Приложение будет доступно по адресу: http://localhost:8000

## Пользователи системы

- **Инженеры**: регистрация дефектов, обновление информации
- **Менеджеры**: назначение задач, контроль сроков, формирование отчётов  
- **Руководители и заказчики**: просмотр прогресса и отчётности

## Технологический стек

### Backend
- Python 3.11+
- Django 4.2+ (Web Framework)
- Django REST Framework (API)
- PostgreSQL (СУБД)


### Frontend  
- React 18+ (UI Framework)
- TypeScript (Типизация)
- Material-UI (Компоненты)
- Axios (HTTP клиент)


### DevOps
- Docker & Docker Compose (Контейнеризация)
- GitHub Actions (CI/CD)


## Архитектура проекта

```
defect-management-system/
├── backend/                 # Django backend
│   ├── apps/               # Приложения Django
│   │   ├── users/         # Пользователи и авторизация
│   │   ├── projects/      # Управление проектами
│   │   ├── defects/       # Управление дефектами
│   │   └── reports/       # Отчеты и аналитика
│   ├── config/            # Настройки проекта
│   ├── requirements.txt   # Python зависимости
│   └── manage.py
├── frontend/               # React frontend
│   ├── src/
│   │   ├── components/    # Компоненты React
│   │   ├── pages/         # Страницы приложения
│   │   ├── services/      # API сервисы
│   │   └── utils/         # Утилиты
│   ├── package.json
│   └── tsconfig.json
├── docs/                   # Документация
├── tests/                  # Тесты
├── docker-compose.yml      # Docker конфигурация
└── .github/workflows/      # CI/CD пайплайны
```


## Текущий статус 

### Что реализовано:
- Базовая архитектура Django backend
- Настройка PostgreSQL и Redis
- Структура React frontend с TypeScript
- Основные модели данных (пользователи, проекты, дефекты)
- Базовый дашборд с метриками
- Docker конфигурация для разработки
- Система миграций базы данных
- Переключение темы светлая/темная

### В разработке (следующие этапы):
- Система аутентификации
- CRUD операции для дефектов
- Управление проектами
- Файловые вложения
- Система уведомлений
- Отчетность и аналитика

## Безопасность

- Хеширование паролей с использованием bcrypt
- Аутентификация через JWT токены
- Логирование действий пользователей
- Автоматическое резервное копирование БД


