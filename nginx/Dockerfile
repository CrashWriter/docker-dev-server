FROM nginx:1.21.4-alpine

WORKDIR /var/www/html

RUN apk --no-cache update;
RUN apk --no-cache upgrade;

RUN apk add --no-cache bash;
RUN apk add --no-cache nano;

RUN echo "Europe/Vienna" > /etc/timezone && \
ln -sf /usr/share/zoneinfo/Europe/Vienna /etc/localtime

COPY .bashrc /root/.bashrc