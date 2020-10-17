FROM php:7.3-fpm

ENV TZ=Asia/Shanghai

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd  \
    && docker-php-ext-install -j$(nproc) gd

RUN pecl install redis-5.1.1 \
    && pecl install xdebug-2.8.1 \
    && pecl install swoole \
    && docker-php-ext-enable redis xdebug swoole

#启动php-fpm