FROM debian:7.5

MAINTAINER Enrique Perez Arnaud <enrique@cazalla.net>

RUN apt-get update && apt-get install -y \
  vim \
  sudo \
  build-essential \
  libreadline-dev \
  zlib1g-dev \
  libpng++-dev \
  libjpeg-dev \
  libfreetype6-dev \
  libncurses-dev \
  libbz2-dev \
  libcrypto++-dev \
  libssl-dev \
  libdb-dev \
  sqlite3 \
  libsqlite3-dev

RUN apt-get install -y locales

RUN DEBIAN_FRONTEND=noninteractive dpkg-reconfigure locales && \
    locale-gen C.UTF-8 && \
    /usr/sbin/update-locale LANG=C.UTF-8

ENV LANG C.UTF-8
ENV LANGUAGE C.UTF-8
ENV LC_ALL C.UTF-8

RUN apt-get install -y wget

RUN wget --no-check-certificate https://www.python.org/ftp/python/3.4.1/Python-3.4.1.tgz \
  && tar xzf Python-3.4.1.tgz \
  && cd Python-3.4.1 \
  && ./configure \
  && make install \
  && cd .. \
  && rm -rf Python-3.4.1*
