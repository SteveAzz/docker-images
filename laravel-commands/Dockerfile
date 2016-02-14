FROM phusion/baseimage
MAINTAINER Steve Azzopardi steveazz@outlook

CMD ["/sbin/my_init"]

RUN apt-get install curl

RUN add-apt-repository ppa:ondrej/php5-5.6
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 4F4EA0AAE5267A6C
RUN apt-key update && apt-get update && apt-get install -y \
    php5 \
    php5-mhash \
    php5-mcrypt \
    php5-curl \
    php5-cli \
    php5-mysql \
    php5-gd \
    php5-intl

RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer

RUN apt-get clean
