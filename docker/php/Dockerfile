FROM php:8-fpm

ENV APP_ENV dev
ENV APP_DEBUG 1

RUN apt-get update && \
    apt-get install -y libicu-dev curl git && \
    curl -sS --insecure https://get.symfony.com/cli/installer | bash && \
    mv /root/.symfony/bin/symfony /usr/local/bin/symfony && \
    docker-php-ext-install mysqli pdo pdo_mysql intl

WORKDIR /usr/local/apache2/htdocs