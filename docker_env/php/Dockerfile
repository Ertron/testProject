FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
        libmcrypt-dev \
        && apt-get install -y libpq-dev libonig-dev
RUN docker-php-ext-install exif
RUN docker-php-ext-install opcache

RUN docker-php-ext-install pdo pdo_mysql mysqli mbstring

ADD php.ini /usr/local/etc/php/conf.d/40-custom.ini

WORKDIR /var/www

CMD ["php-fpm"]
