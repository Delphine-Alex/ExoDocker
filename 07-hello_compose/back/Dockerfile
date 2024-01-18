FROM node:18-alpine

WORKDIR /07-hello_compose

COPY . .

RUN npm install

EXPOSE 3000 

CMD ["node", "server.js"]