FROM php:7.2-fpm-alpine
RUN apk add --no-cache bash
CMD ["php-fpm"]
COPY ./www.conf /usr/local/etc/php-fpm.d/www.conf
COPY ./index.php /app/index.php

