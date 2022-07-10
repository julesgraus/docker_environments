FROM php:8.1-alpine
WORKDIR /usr/src/app
RUN apk update
RUN apk add --no-cache libpng libpng-dev
RUN apk add zlib
RUN docker-php-ext-install gd
RUN docker-php-ext-configure gd
RUN docker-php-ext-install pdo
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-configure pdo_mysql
RUN docker-php-ext-install sockets
RUN docker-php-ext-configure sockets
RUN docker-php-ext-configure spl
RUN docker-php-ext-install bcmath
RUN docker-php-ext-configure bcmath
RUN docker-php-ext-install ctype
RUN docker-php-ext-configure ctype
RUN docker-php-ext-install fileinfo
RUN docker-php-ext-configure fileinfo
RUN docker-php-ext-configure json
RUN pecl install redis-5.3.7
RUN pecl install xdebug-3.1.5
RUN docker-php-ext-enable redis xdebug
COPY "./configuration/php.ini-development" "$PHP_INI_DIR/php.ini"
