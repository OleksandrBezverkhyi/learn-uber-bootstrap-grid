# Finora — Project structure



## Finora — мінімальна структура проєкту

Нижче — стислий огляд основних директорій та необхідних файлів. Коментарі українською.

```
finora/
├─ app/                 # Маршрути та сторінки
│  ├─ layout.js         # Загальний лейаут (провайдери, шрифти)
│  ├─ globals.css       # Глобальні стилі
│  ├─ page.js           # Публічна головна сторінка
│  ├─ (public)/         # Публічні маршрути (login, register)
│  └─ (protected)/      # Захищені маршрути (dashboard, transactions тощо)
├─ app/api/             # API-ендпоінти (auth, transactions, import/export, analytics)
├─ components/          # UI-компоненти та блоки інтерфейсу
├─ lib/                 # Серверні утиліти та бізнес-логіка (DB, валідатори, хелпери)
├─ prisma/              # Схема БД та міграції (schema.prisma, seed)
├─ public/              # Статичні файли (логотипи, іконки, зображення)
├─ docs/                # Документація та діаграми
├─ schemas/             # Загальні схеми валідації (Zod)
├─ hooks/               # Користувацькі React-хуки
├─ types/               # Глобальні типи/інтерфейси (TS)
├─ package.json         # Залежності та npm-скрипти
├─ next.config.mjs      # Конфігурація Next.js
├─ postcss.config.mjs   # Налаштування CSS-білду
├─ tailwind.config.mjs  # Налаштування Tailwind
├─ README.md            # Опис проекту та інструкції
├─ .env                 # Змінні оточення (не комітити)
└─ PROJECT_STRUCTURE.md  # Цей файл

```

### Візуальна діаграма (стилізована)

```
[Користувацький інтерфейс]
	│
	├─ app/ (pages: public / protected)
	│
	├─ components/  → UI-блоки
	│
	└─ app/api/     → Серверні ендпоінти

[Сервер/логіка]
	├─ lib/         → бізнес-логіка, утиліти
	├─ prisma/      → модель БД
	└─ schemas/     → валідація даних

[Ресурси]
	├─ public/      → статичні файли
	└─ docs/        → документація

```



