FROM php:7.4-apache

RUN apt-get update && \
    apt-get install -y nano vim tree git libzip-dev zip gnupg && \
    docker-php-ext-configure zip && \
    docker-php-ext-install zip && \
    docker-php-ext-install pdo_mysql && \
    docker-php-ext-install mysqli && \
    docker-php-ext-install bcmath && \
    pecl install xdebug && \
    docker-php-ext-enable xdebug 

RUN curl --silent --show-error https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer