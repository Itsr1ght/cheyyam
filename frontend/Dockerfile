FROM oven/bun:1.4.2-alpine

WORKDIR /app

COPY package.json bun.lock /app/
RUN bun install

COPY . /app
EXPOSE 3000

CMD ["/usr/local/bin/bun", "run", "dev"]
