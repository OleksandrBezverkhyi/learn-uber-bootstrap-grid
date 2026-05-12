# Finora — Project structure

app/ — Next.js routes and pages
  (protected)/ — pages for authenticated users (dashboard, transactions, profile)
  (public)/ — public pages (login, register)

app/api/ — server API routes (auth, transactions, categories, import/export, analytics)

components/ — React UI components grouped by feature

lib/ — server-side utilities and business logic (DB client, validators, helpers)

prisma/ — database schema and migrations (schema.prisma, seed, migrations)

docs/ — documentation and diagrams (manuals, ER diagram)

package.json — project metadata, scripts and dependencies

postcss.config.mjs, tailwind config — styling build config

README.md — project overview and setup instructions

.env (not committed) — environment variables (DATABASE_URL, secrets)

.next/, node_modules/ — build and dependency folders (generated)
