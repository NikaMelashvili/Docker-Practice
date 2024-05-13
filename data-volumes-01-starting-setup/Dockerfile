FROM node:14

WORKDIR /app

# we can also use /app instead of the . but we have the WORKDIR set so we can use .
COPY package.json . 

RUN npm install

# in here the first . referes to the content and the second . refers to the WORKDIR
COPY . .

EXPOSE 80

# volumes help manage data
VOLUME [ "/app/feedback" ]

CMD [ "node", "server.js" ]