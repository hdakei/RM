FROM nginx

COPY ./content/index.html /usr/share/nginx/html/index.html

COPY ./config/nginx.conf /etc/nginx/nginx.conf

COPY ./config/default.conf /etc/nginx/conf.d/default.conf
RUN mkdir /usr/share/nginx/html/php

COPY ./content/index.php /app/index.php
COPY ./content/index.php /usr/share/nginx/html/php/index.php


VOLUME /usr/share/nginx/html/php
VOLUME /usr/share/nginx/html
VOLUME /etc/nginx

