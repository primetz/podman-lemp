FROM docker.io/library/nginx:1.20.1

ARG USER_ID
ARG GROUP_ID

WORKDIR /var/www

RUN usermod -u ${USER_ID} www-data && \
    groupmod -g ${GROUP_ID} www-data