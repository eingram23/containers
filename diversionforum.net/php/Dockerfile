# Filename: Dockerfile
FROM php:7.4.32-fpm

COPY php.ini /usr/local/etc/php/

RUN apt-get update -y && apt-get install -y libonig-dev sendmail libpng-dev libmagickwand-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
RUN docker-php-ext-install mysqli mbstring exif
RUN printf "\n" | pecl install imagick
RUN docker-php-ext-enable imagick

# RUN docker-php-ext-install gd
