FROM node:18-alpine

WORKDIR /04-hello_docker_node

COPY . .

RUN npm install

EXPOSE 3000 

CMD ["node", "server.js"]

