FROM nginx:alpine

ADD nginx/nginx.conf /etc/nginx/
ADD nginx/sites-available/*.conf /etc/nginx/sites-available/

#RUN set -x ; \
#    addgroup -g 82 -S www-data ; \
#    adduser -u 82 -D -S -G www-data www-data && exit 0 ; exit 1

WORKDIR /var/www/laravel-six