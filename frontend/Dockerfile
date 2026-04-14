FROM node:18
WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm install

COPY . .
RUN npm run build

# Убираем запуск сервера - статику будет раздавать Nginx
# Команда будет переопределена в docker-compose.yml
CMD ["echo", "Frontend build completed. Static files are ready to be copied."]
