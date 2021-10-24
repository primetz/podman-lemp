FROM docker.io/library/mysql:8.0

ARG USER_ID
ARG GROUP_ID

RUN usermod -u ${USER_ID} mysql && \
    groupmod -g ${GROUP_ID} mysql