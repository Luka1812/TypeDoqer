FROM php:7.2-fpm

RUN apt-get update

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/laravel-six

#LIB_XML#
ARG INSTALL_LIB_XML

RUN if [ ${INSTALL_LIB_XML} = true ]; then \
    apt install -y libxml2-dev \
;fi
#########################

#OPENSSL#
ARG INSTALL_OPEN_SSL

RUN if [ ${INSTALL_OPEN_SSL} = true ]; then \
    apt install -y openssl \
;fi
#########################

#PDO#
ARG INSTALL_PDO

RUN if [ ${INSTALL_PDO} = true ]; then \
    docker-php-ext-install pdo pdo_mysql \
;fi
#########################

#SOCKET#
ARG INSTALL_SOCKET

RUN if [ ${INSTALL_SOCKET} = true ]; then \
    docker-php-ext-install sockets \
;fi
#########################

#JSON#
ARG INSTALL_JSON

RUN if [ ${INSTALL_JSON} = true ]; then \
    docker-php-ext-install json \
;fi
#########################

#SOAP#
ARG INSTALL_SOAP

RUN if [ ${INSTALL_SOAP} = true ]; then \
    docker-php-ext-install soap \
;fi
#########################

#MBSTRING#
ARG INSTALL_MBSTRING

RUN if [ ${INSTALL_MBSTRING} = true ]; then \
    docker-php-ext-install mbstring \
;fi
#########################

#MAIL PARSE#
ARG INSTALL_MAIL_PARSE

RUN if [ ${INSTALL_MAIL_PARSE} = true ]; then \
    pecl install -o -f mailparse \
    &&  rm -rf /tmp/pear \
    && docker-php-ext-enable mailparse \
;fi
#########################

#NODE#
ARG INSTALL_NODE

RUN if [ ${INSTALL_NODE} = true ]; then \
  apt-get install -y curl \
  && curl -sL https://deb.nodesource.com/setup_9.x | bash - \
  && apt-get install -y nodejs \
  && curl -L https://www.npmjs.com/install.sh | sh \
;fi
#########################

#NODE#
ARG INSTALL_SASS

RUN if [ ${INSTALL_SASS} = true ]; then \
  npm install node-sass \
;fi
#########################


RUN apt-get install -y sendmail libpng-dev
RUN docker-php-ext-install gd




