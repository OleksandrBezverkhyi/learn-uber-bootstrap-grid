# Finora — Project structure

```
finora/
├── app/                                # Next.js App Router (маршрутизація)
│   ├── layout.js                       # Кореневий лейаут (шрифти, провайдери)
│   ├── globals.css                     # Глобальні стилі
│   ├── page.js                         # Публічна головна сторінка
│   ├── (public)/                       # Маршрути для неавторизованих користувачів
│   │   ├── login/
│   │   │   └── page.js                 # Сторінка входу
│   │   └── register/
│   │       └── page.js                 # Сторінка реєстрації
│   └── (protected)/                    # Приватні маршрути (вимагають автентифікації)
│       ├── layout.js                   # Layout для захищених сторінок
│       ├── dashboard/
│       │   └── page.js                 # Dashboard overview
│       ├── transactions/
│       │   └── page.js                 # Управління транзакціями (список, фільтри)
│       ├── budgets/
│       │   └── page.js                 # Сторінка бюджетів
│       ├── categories/
│       │   └── page.js                 # Сторінка категорій
│       ├── goals/
│       │   └── page.js                 # Сторінка цілей
│       ├── import-export/
│       │   └── page.js                 # Імпорт/експорт даних UI
│       └── profile/
│           └── page.js                 # Налаштування профілю
│
├── app/api/                            # API‑роути (edge/route handlers)
│   ├── auth/
│   │   └── [...nextauth]/route.js      # next-auth handlers (signin, session)
│   ├── auth/
│   │   └── register/route.js           # реєстрація користувача
│   ├── transactions/
│   │   ├── route.js                    # GET/POST transactions
│   │   └── [id]/route.js               # GET/PUT/DELETE transaction by id
│   ├── categories/
│   │   ├── route.js
│   │   └── [id]/route.js
│   ├── budgets/
│   │   ├── route.js
│   │   └── [id]/route.js
│   ├── goals/
│   │   ├── route.js
│   │   └── [id]/route.js
│   ├── import/
│   │   └── csv/route.js                # CSV import endpoint
│   ├── export/
│   │   └── csv/route.js                # CSV export endpoint
│   ├── analytics/
│   │   ├── summary/route.js
│   │   ├── by-category/route.js
│   │   └── trend/route.js
│   └── profile/
│       ├── route.js
│       └── reset/route.js
│
├── components/                         # React UI components (feature folders)
│   ├── auth/
│   │   ├── login-form.js
│   │   └── register-form.js
│   ├── transactions/
│   │   └── transactions-manager.js
│   ├── categories/
│   │   └── categories-manager.js
│   ├── budgets/
│   │   └── budgets-manager.js
│   ├── goals/
│   │   └── goals-manager.js
│   ├── analytics/
│   │   └── analytics-overview.js
│   ├── dashboard/
│   │   └── dashboard-overview.js
│   ├── profile/
│   │   └── profile-settings.js
│   └── common/
│       ├── app-shell.js
│       ├── container.js
│       ├── day-first-date-input.js
│       ├── locale-provider.js
│       ├── locale-switcher.js
│       ├── nav-links.js
│       └── sign-out-button.js
│
├── hooks/                              # Custom React hooks
│   ├── useAuth.js
│   ├── useDebounce.js
│   └── useLocalStorage.js
│
├── lib/                                # Серверні утиліти та бізнес-логіка
│   ├── prisma.js                       # Prisma client wrapper
│   ├── auth.js                         # Auth helpers / callbacks
│   ├── session.js                      # Session helpers
│   ├── csv.js                          # CSV build/parse helpers
│   ├── transactions.js                 # Domain logic for transactions
│   ├── budgets.js
│   ├── goals.js
│   ├── analytics.js
│   ├── recommendations.js
│   ├── date.js
│   ├── validators.js                   # Zod schemas used server/client
│   └── i18n.js                         # Localization strings / helpers
│
├── schemas/                            # Zod validation schemas (shared)
│   ├── transaction.schema.ts
│   ├── auth.schema.ts
│   └── profile.schema.ts
│
├── types/                              # TypeScript global types / interfaces
│   ├── index.d.ts
│   └── api.d.ts
│
├── prisma/                             # Database schema & migrations
│   ├── schema.prisma
│   ├── seed.js
│   └── migrations/
│
├── public/                             # Static assets
│   ├── images/
│   ├── icons/
│   └── favicon.ico
│
├── docs/                               # Документація, діаграми, manuals
│   ├── manual-checks.md
│   └── er-diagram.svg
│
├── scripts/                            # Dev / maintenance scripts (optional)
│   └── import-sample-data.js
│
├── .env                                # Environment variables (not committed)
├── .gitignore
├── next.config.mjs
├── package.json
├── postcss.config.mjs
├── tailwind.config.mjs
├── README.md
└── PROJECT_STRUCTURE.md                # (this file)

```

