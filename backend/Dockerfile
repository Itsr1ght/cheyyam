FROM ghcr.io/astral-sh/uv:python3.12-alpine AS builder

ENV UV_COMPILE_BYTECODE=1

WORKDIR /app

COPY pyproject.toml uv.lock ./
RUN uv sync --frozen --no-dev

COPY ./src /app
EXPOSE 8000

CMD [ "uv", "run", "python", "manage.py", "runserver" ]
