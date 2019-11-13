FROM php:fpm-alpine
RUN docker-php-ext-install pdo pdo_mysql

RUN docker-php-ext-install gd

CMD ["php-fpm"]

EXPOSE 9000
