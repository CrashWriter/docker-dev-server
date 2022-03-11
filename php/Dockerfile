FROM php:8.0-fpm-alpine

WORKDIR /var/www/html

RUN apk --no-cache update;
RUN apk --no-cache upgrade;

RUN apk add --no-cache bash;
RUN apk add --no-cache nano;
RUN apk add --no-cache icu-dev;

RUN docker-php-ext-configure intl \
    && docker-php-ext-install intl \
        mysqli \
        pdo \
        pdo_mysql \
    && docker-php-ext-enable intl;

RUN rm -rf /tmp/* /usr/local/lib/php/doc/* /var/cache/apk/*;

RUN echo "Europe/Vienna" > /etc/timezone && \
ln -sf /usr/share/zoneinfo/Europe/Vienna /etc/localtime

COPY .bashrc /root/.bashrc