FROM node:12

RUN git clone https://github.com/z0BI7z/alerha-server.git /server

COPY ./.env ./server

WORKDIR /server

RUN npm i

RUN npm run compile

CMD [ "npm", "start" ]