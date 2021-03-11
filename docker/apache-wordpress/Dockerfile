FROM php:7-apache

RUN php -m
RUN apt-get update && apt-get install -y \ 
        zip libzip-dev libfreetype6-dev libjpeg62-turbo-dev libpng-dev  
RUN docker-php-ext-install exif zip mysqli \
        && docker-php-ext-install -j$(nproc) gd 
RUN php -m