FROM nginx:stable-alpine

RUN apk update && apk add tzdata bash

RUN rm /etc/nginx/conf.d/default.conf

COPY ./config/nginx.conf /etc/nginx/nginx.conf
COPY ./config/robots.txt /etc/nginx/robots.txt
COPY ./config/nginx.htpasswd /etc/nginx/nginx.htpasswd

CMD [ "nginx", "-g", "daemon off;" ]