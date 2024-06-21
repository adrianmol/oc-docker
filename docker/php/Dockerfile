# docker/php/Dockerfile
FROM php:8.3-fpm

RUN apt-get update && apt-get install -y \
    build-essential \
    libpng-dev \
    libjpeg-dev \
    libwebp-dev \
    libxpm-dev \
    libjpeg62-turbo-dev \
    libfreetype6-dev \
    locales \
    zip \
    libzip-dev \
    zlib1g \
    jpegoptim optipng pngquant gifsicle \
    vim \
    unzip \
    git \
    curl \
    apache2 \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install -j$(nproc) zip \
    && docker-php-ext-install pdo_mysql exif pcntl mysqli

#RUN apt-get update && apt-get install -y \
#    git \
#    curl \
#    libpng-dev \
#    libonig-dev \
#    libxml2-dev \
#    zlib1g-dev \
#    libjpeg-dev
#
#RUN docker-php-ext-configure gd
#
#RUN apt-get update && \
#    apt-get install -y \
#    libzip-dev \
#    && docker-php-ext-install zip \
#    && docker-php-ext-install gd \
#    && docker-php-ext-install mysqli