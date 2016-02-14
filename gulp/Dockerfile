FROM phusion/baseimage
MAINTAINER Steve Azzopardi steveazz@outlook

CMD ["/sbin/my_init"]

RUN apt-get install curl

RUN curl --silent --location https://deb.nodesource.com/setup_4.x | bash -

RUN apt-get install --yes nodejs

RUN npm install npm -g

RUN npm install gulp -g

RUN apt-get clean
