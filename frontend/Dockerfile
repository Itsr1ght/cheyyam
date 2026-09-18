FROM oven/bun:1.3.11-alpine

WORKDIR /app

COPY package.json bun.lock /app/
RUN bun install --frozen-lockfile

COPY . /app
EXPOSE 5173

CMD [ "bun", "start"]
