FROM php:fpm-alpine
RUN docker-php-ext-install pdo pdo_mysql

RUN apk add --no-cache \
		libpng-dev \
		libjpeg-turbo-dev \
	&& docker-php-ext-configure gd --with-jpeg-dir=/usr/include/ \
	&& docker-php-ext-install gd && apk del libpng-dev libjpeg-turbo-dev

CMD ["php-fpm"]

EXPOSE 9000
