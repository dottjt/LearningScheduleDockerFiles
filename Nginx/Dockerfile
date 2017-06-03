FROM alpine:latest

RUN apk update && apk upgrade && apk add --update nginx openrc && rm -rf /var/cache/apk/*

COPY ./default.conf /etc/nginx/conf.d/default.conf

RUN rc-update add nginx default

CMD rc-service nginx start
