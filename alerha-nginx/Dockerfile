FROM node:12

COPY ./alerha-client /app

WORKDIR /app

RUN npm i

RUN npm run build

FROM nginx

COPY --from=0 /app/build /client

WORKDIR /etc/nginx/conf.d

RUN rm default.conf

COPY nginx.conf default.conf