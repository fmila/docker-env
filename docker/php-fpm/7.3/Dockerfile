# php-fpm
FROM php:7.3-fpm

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
        libsqlite3-dev \
        libssl-dev \
        libcurl3-dev \
        libxml2-dev \
    && docker-php-ext-install iconv json mbstring mysqli pdo_mysql pdo_sqlite curl ftp hash session simplexml tokenizer xml xmlrpc  \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd

CMD ["php-fpm"]

EXPOSE 9000