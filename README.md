# Contacts CRUD API

A REST API for managing personal contacts, built with FastAPI, async SQLAlchemy, and PostgreSQL.

## Features

- CRUD operations for contacts (create, read, update, delete)
- Search contacts by first name, last name, or email
- List contacts with upcoming birthdays
- Async PostgreSQL access via SQLAlchemy + asyncpg
- Database migrations with Alembic

## Stack

- Python 3, FastAPI
- SQLAlchemy (async), PostgreSQL, Alembic

## Setup

1. Install dependencies:
   ```bash
   poetry install
   ```
2. Create a `.env` file with the database connection settings (see `conf/config.py`).
3. Apply database migrations:
   ```bash
   poetry run alembic upgrade head
   ```

## Usage

```bash
poetry run uvicorn main:app --host 127.0.0.1 --port 8000 --reload
```

Interactive API docs are available at `/docs` once the server is running.
