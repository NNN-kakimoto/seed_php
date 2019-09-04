FROM php:7.2-apache

COPY ./php.ini /usr/local/etc/php/
COPY ./default.conf /etc/apache2/sites-enabled/

RUN apt-get update \
  && apt-get install -y zlib1g-dev libpq-dev mariadb-client unzip\
  && docker-php-ext-install zip pdo_mysql mysqli \
  && docker-php-ext-enable mysqli vim 

WORKDIR /var/www

EXPOSE 80
CMD ["apachectl", "-D", "FOREGROUND"]