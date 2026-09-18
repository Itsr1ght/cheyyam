FROM oven/bun:1.3.11-alpine

WORKDIR /app

COPY package.json bun.lock /app/
RUN bun install

COPY . /app
EXPOSE 3000

CMD [ "bun", "start"]
