FROM node:12

ENV PORT=3000
ENV MONGODB_URI=mongodb://mongo:27017/alerha
ENV REACT_APP_API_URL=http://localhost:8080

COPY ./alerha-client /client
COPY ./alerha-server /server

WORKDIR /client

RUN npm i

RUN npm run build

WORKDIR /server

RUN npm i

RUN npm run compile

RUN mv /client/build /server/dist/client

CMD [ "npm", "start" ]