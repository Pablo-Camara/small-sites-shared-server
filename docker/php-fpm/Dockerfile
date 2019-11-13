FROM php:fpm-alpine
RUN docker-php-ext-install pdo pdo_mysql

RUN apk add --no-cache libpng libpng-dev && docker-php-ext-install gd && apk del libpng-dev

CMD ["php-fpm"]

EXPOSE 9000
