FROM oven:/bun:1.0-alpine AS builder

WORKDIR /app

COPY package.json bun.lockb /app/
RUN bun install --frozen-lockfile
COPY . /app/
EXPOSE 5173
CMD [ "bun", "run", "dev", "host" ]
