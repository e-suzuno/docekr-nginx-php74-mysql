FROM php:7.4-fpm

RUN apt-get update



RUN usermod -u 1000 www-data -s /bin/bash && groupmod -g 1000 www-data


RUN apt-get install -y automake autoconf \
 pngquant libpng-dev libxrender1 libfontconfig libxext6 fonts-ipafont \
 curl vim wget libzip-dev libpq-dev


# pdo
RUN docker-php-ext-install pdo pdo_mysql pdo_pgsql gd zip


# composer
WORKDIR /tmp
RUN wget https://getcomposer.org/composer.phar
RUN mv composer.phar /bin/composer
RUN chmod 700 /bin/composer



# nodejs, npm
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash - \
 && apt-get install -y nodejs
RUN nodejs -v && npm -v
# for nodejs update
RUN npm -g install n
RUN n --version
RUN n stable
RUN nodejs -v && node -v && npm -v



# xdebug
RUN pecl install xdebug \
  && docker-php-ext-enable xdebug


# web root
WORKDIR /var/www/html


