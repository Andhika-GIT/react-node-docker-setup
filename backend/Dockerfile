FROM node:14

ARG DEFAULT_MONGO_HOST=localhost

WORKDIR /app

COPY package*.json .

RUN npm install

COPY . .

ENV MONGO_DB_HOST=${DEFAULT_MONGO_HOST}

EXPOSE 80

CMD [ "node", "app.js" ]