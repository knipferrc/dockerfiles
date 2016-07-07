FROM debian:latest

MAINTAINER knipferrc <knipferrc@gmail.com>

RUN apt-get update && apt-get install -y \
    curl \
    git \
    wget \
    sudo \
    nano \
    vim \
    python3 \
    build-essential \
    tar \
    locales

RUN locale-gen en_US.UTF-8

RUN curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash - \
  && apt-get install nodejs -y \
  && curl https://install.meteor.com/ | sh \
  && wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh \
  && curl -O https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz \
  && tar -xvf go1.6.2.linux-amd64.tar.gz \
  && mv go /usr/local \
  && rm -r go1.6.2.linux-amd64.tar.gz

ENV PATH=$PATH:/usr/local/go/bin

RUN adduser --disabled-password --gecos '' devbox

USER devbox

WORKDIR /home/devbox
