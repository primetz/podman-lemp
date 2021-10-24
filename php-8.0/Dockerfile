FROM docker.io/library/php:8.0-fpm

ARG USER_ID
ARG GROUP_ID

WORKDIR /var/www

RUN docker-php-ext-install mysqli

RUN usermod -u ${USER_ID} www-data && \
    groupmod -g ${GROUP_ID} www-data

USER "${USER_ID}:${GROUP_ID}"