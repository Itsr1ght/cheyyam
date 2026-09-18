FROM ghcr.io/astral-sh/uv:python3.12-alpine

ENV UV_COMPILE_BYTECODE=1
ENV UV_LINK_MODE=copy

WORKDIR /app

COPY pyproject.toml uv.lock ./
RUN uv sync --frozen --no-dev

COPY . /app
EXPOSE 8000

CMD [ "uv", "run", "python", "manage.py", "runserver" ]
