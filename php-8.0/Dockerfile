FROM docker.io/library/php:8.0-fpm

ARG USER_ID
ARG GROUP_ID

WORKDIR /var/www

RUN apt-get update \
    && apt-get install -y g++ git vim zlib1g-dev libicu-dev libzip-dev zip \
    && docker-php-ext-install intl pdo pdo_mysql \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

ADD ./php.ini /usr/local/etc/php/php.ini
ADD ./docker-php-ext-xdebug.ini /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini

RUN usermod -u ${USER_ID} www-data && \
    groupmod -g ${GROUP_ID} www-data

USER "${USER_ID}:${GROUP_ID}"