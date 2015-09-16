FROM debian:jessie

MAINTAINER WHITEPLUS System "sysadmin@wh-plus.com"

ENV NGINX_VERSION 1.9.4-1~jessie

RUN apt-key adv --keyserver hkp://pgp.mit.edu:80 --recv-keys 573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62
RUN echo "deb http://nginx.org/packages/mainline/debian/ jessie nginx" >> /etc/apt/sources.list

RUN /bin/cp -f /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
 && apt-get update \
 && apt-get upgrade -y \
 && apt-get install -y \
 ca-certificates nginx=${NGINX_VERSION} supervisor curl git \
 php5-fpm php5-mysql php-apc php5-curl php5-gd php5-intl php5-mcrypt php5-memcache \
 php5-sqlite php5-tidy php5-xmlrpc php5-xsl php5-pgsql php5-mongo libapache2-mod-php5 \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*
