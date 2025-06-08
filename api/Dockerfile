FROM node:18-alpine

WORKDIR /app

# Копируем зависимости
COPY package.json ./
# Если есть — тоже добавь:
COPY package-lock.json ./

# Устанавливаем зависимости
RUN npm install
RUN npm install -g nodemon
# Копируем остальной код
COPY . .

# Запускаем приложение
CMD ["npm", "run", "dev"]
