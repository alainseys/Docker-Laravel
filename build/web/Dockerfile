FROM php:7.2-apache
RUN rm /etc/apt/preferences.d/no-debian-php
RUN apt-get update \
&& apt-get install php-dom -y \ 
&& apt-get install composer -y \
&& apt-get install zip -y \
&& apt-get install libxml2-dev -y \
&& apt-get install -y vim git zlib1g-dev mariadb-client libzip-dev \
&& docker-php-ext-install zip mysqli pdo_mysql  zip mbstring xml  \
&& docker-php-ext-install dom 
#&& docker-php-ext-install xdebug 
RUN apt-get install php-zip -y
RUN apt-get install curl -y
RUN docker-php-ext-install pdo  mbstring 
RUN php -v
RUN composer -v
RUN apt-get purge nodejs -y
RUN apt-get install sudo -y
RUN curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
RUN apt-get install nodejs -y
RUN echo NodeJs is installed.
RUN a2enmod rewrite
RUN service apache2 restart
WORKDIR /var/www/html
EXPOSE 80