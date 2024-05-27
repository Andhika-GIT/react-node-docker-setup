FROM node:14

WORKDIR /app

COPY package*.json .

RUN npm install

COPY . .

ENV MONGO_DB_HOST=mongo_c
ENV MONGO_DB_USERNAME=hubla_goals_username
ENV MONGO_DB_PASSWORD=hubla_goals_password

EXPOSE 80

CMD [ "node", "app.js" ]