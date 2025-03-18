# base
FROM node:16

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install && npm install -g serve

COPY . .

ENV REACT_APP_BACKEND_URL=http://localhost/api

RUN npm run build

EXPOSE 5000

CMD ["serve","-s","-l","5000","build"]

