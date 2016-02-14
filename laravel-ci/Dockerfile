FROM php:7
MAINTAINER Steve Azzopardi steveazz@outlook

RUN apt-get update -yqq

# Install git
RUN apt-get install git -yqq

# Install composer and make it globaly avaible
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer

# Install mysql pdo
RUN docker-php-ext-install pdo_mysql

# Install mbstring
RUN docker-php-ext-install mbstring

# Instal mtcrypts
RUN apt-get install -y libmcrypt-dev \
    && docker-php-ext-install mcrypt

# Install zip
RUN apt-get install -y zlib1g-dev \
    && pecl install zip \
    && docker-php-ext-enable zip

# Install nodejs
RUN curl -sL https://deb.nodesource.com/setup_4.x | bash - \
    && apt-get install -y nodejs

# Update npm
RUN npm install npm -g

# Install gulp
RUN npm install gulp -g

# Clear cache
RUN apt-get clean
