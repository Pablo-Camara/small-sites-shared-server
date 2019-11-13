FROM php:fpm-alpine
RUN docker-php-ext-install pdo pdo_mysql

RUN apk add --no-cache libpng libpng-dev libjpeg libjpeg-turbo-dev
RUN docker-php-ext-configure gd \
        --with-png-dir=/usr/lib/ \
        --with-jpeg-dir=/usr/lib/ \
        --with-gd
RUN docker-php-ext-install gd
RUN apk del libpng-dev libjpeg-turbo-dev

CMD ["php-fpm"]

EXPOSE 9000
