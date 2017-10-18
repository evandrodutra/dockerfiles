FROM jupyter/minimal-notebook

MAINTAINER Evandro Dutra <evandro.eld@gmail.com>

USER root

RUN apt-get update && apt-get install -yq \
    libtool \
    libffi-dev \
    ruby \
    ruby-dev \
    make \
    git \
    libzmq-dev \
    autoconf \
    pkg-config \
    && apt-get clean && cd ~ \
    rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/zeromq/czmq \
    cd czmq \
    ./autogen.sh && ./configure && sudo make && sudo make install

USER $NB_USER

RUN gem install cztop iruby \
    iruby register --force
