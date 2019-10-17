FROM php:7.2-fpm

RUN apt-get update \
&& apt install -y libxml2-dev  \
&& apt install -y openssl  \
&& docker-php-ext-install pdo pdo_mysql

RUN docker-php-ext-install json \
&& docker-php-ext-install soap \
&& docker-php-ext-install mbstring \
&& pecl install -o -f mailparse \
&&  rm -rf /tmp/pear \
&& docker-php-ext-enable mailparse

#INSTALL SOCKET EXTENSION#
ARG INSTALL_PHP_SOCKET

RUN if [ ${INSTALL_PHP_SOCKET} = true ]; then \
    docker-php-ext-install sockets \
;fi
#########################

