FROM node:18-alpine

# 1. Устанавливаем рабочую директорию
WORKDIR /app

# 2. Копируем только зависимости
COPY package.json ./
# Если есть package-lock.json, раскомментируй:
# COPY package-lock.json ./

# 3. Устанавливаем зависимости
RUN npm install

# 4. Устанавливаем nodemon глобально (можно опустить и использовать локально)
RUN npm install -g nodemon

# 5. Копируем всё остальное
COPY . .

# 6. Указываем порт
EXPOSE 5000

# 7. Запуск
CMD ["npm", "run", "dev"]

