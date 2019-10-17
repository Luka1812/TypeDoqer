FROM php:7.2-fpm

RUN apt-get update \
&& apt install -y libxml2-dev  \

&& docker-php-ext-install pdo pdo_mysql \
&& docker-php-ext-install sockets \
&& docker-php-ext-install json \
&& docker-php-ext-install soap \


&& pecl install -o -f mailparse \
&&  rm -rf /tmp/pear \
&& docker-php-ext-enable mailparse


