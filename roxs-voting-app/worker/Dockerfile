FROM node:lts-iron
WORKDIR /app
COPY package*.json ./
RUN npm install && npm install pm2 -g
COPY . .
EXPOSE 3000
CMD ["pm2-runtime", "start", "main.js", "--name", "vote-worker"]