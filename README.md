# Hi, I'm Vladyslav 👋

Python backend developer based in Poland (CET). I build web services and APIs
with Django and FastAPI on PostgreSQL, and I care most about the parts that are
easy to get wrong: transactions and concurrency, payment flows, and code that
is typed, tested, and documented.

I'm looking for a **Python backend** role, remote or hybrid.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Vladyslav_F.-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vladyslav-f-b3428540a/)

## Projects

### [Ludora](https://github.com/vladyslav-fdnk/ludora) — digital-product marketplace

Django REST API and a Telegram bot for selling license keys, with Stripe
Checkout and webhooks.

- Checkout reserves stock under PostgreSQL row locks, so two buyers can never
  get the same key; multi-threaded tests race real transactions to prove it.
- Idempotent Stripe webhooks that tolerate duplicates and out-of-order events,
  with an [ADR](https://github.com/vladyslav-fdnk/ludora/blob/master/docs/architecture/ADR-001-license-reservation.md)
  documenting the reservation design.
- gunicorn + nginx deployment, Celery on Redis, per-IP rate limiting on auth.
- ~400 tests, 94% coverage, mypy and Ruff in CI.

`Django` `DRF` `PostgreSQL` `Celery` `Redis` `Stripe` `aiogram` `Docker`

### [MintFlow](https://github.com/vladyslav-fdnk/MintFlow) — personal expense tracker

Capture expenses in Telegram, including from a receipt photo; understand them
in a web app with dashboards and multi-currency conversion.

- Modular monolith with a clear domain layer: a draft becomes an expense only
  after explicit confirmation.
- Receipt recognition behind a replaceable interface (Azure AI Document
  Intelligence), magic-link sign-in, ECB and NBU exchange rates.
- Caddy with automatic HTTPS, images published to GHCR, encrypted backups.
- ~1,700 tests, mypy and Ruff in CI.

`FastAPI` `SQLAlchemy` `Alembic` `PostgreSQL` `htmx` `Telegram Bot API` `Docker`

## Toolbox

**Languages:** Python · SQL
**Frameworks:** Django · Django REST Framework · FastAPI · aiogram
**Data:** PostgreSQL · SQLAlchemy · Alembic · Redis · Celery
**Quality:** pytest · mypy · Ruff · pre-commit · GitHub Actions
**Infrastructure:** Docker Compose · nginx · Caddy · Linux

## Contact

The fastest way to reach me is [LinkedIn](https://www.linkedin.com/in/vladyslav-f-b3428540a/).
