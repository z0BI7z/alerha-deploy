FROM node:12

RUN git clone https://github.com/z0BI7z/alerha-client.git /app

COPY ./.env /app

WORKDIR /app

RUN npm i

RUN npm run build

FROM nginx

COPY --from=0 /app/build /client

WORKDIR /etc/nginx/conf.d

RUN rm default.conf

COPY nginx.conf default.conf