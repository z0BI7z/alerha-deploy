FROM node:12

ENV PORT=3000
ENV MONGODB_URI=mongodb://mongo:27017/alerha

RUN git clone https://github.com/z0BI7z/alerha-server.git /server

WORKDIR /server

RUN npm i

RUN npm run compile

CMD [ "npm", "start" ]