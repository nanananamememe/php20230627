FROM php:8.2.7-fpm

RUN apt-get update ;
RUN apt-get install -y git unzip ;
RUN docker-php-ext-install pdo_mysql ;
RUN php -r "touch('/var/www/html/hoge');"
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');";
RUN php composer-setup.php;
RUN mv composer.phar /usr/bin/composer
