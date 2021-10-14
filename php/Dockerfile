FROM php:8.0-fpm-alpine

WORKDIR /var/www/html

RUN apk update;
RUN apk upgrade;

RUN apk add --no-cache bash;
RUN apk add --no-cache nano;

RUN echo "Europe/Vienna" > /etc/timezone && \
ln -sf /usr/share/zoneinfo/Europe/Vienna /etc/localtime

COPY .bashrc /root/.bashrc