FROM docker.io/library/nginx:stable

ARG USER_ID
ARG GROUP_ID

WORKDIR /var/www

RUN usermod -u ${USER_ID} www-data && \
    groupmod -g ${GROUP_ID} www-data
