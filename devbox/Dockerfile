FROM ubuntu:latest

MAINTAINER knipferrc <knipferrc@gmail.com>

RUN apt-get update && apt-get install -y \
    curl \
    git \
    wget \
    sudo \
    nano \
    vim \
    python3 \
    python \
    build-essential \
    tar \
    locales

RUN locale-gen en_US.UTF-8

RUN curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash - \
  && apt-get install nodejs -y \
  && curl https://install.meteor.com/ | sh \
  && wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh \
  && curl -O https://storage.googleapis.com/golang/go1.7.1.linux-amd64.tar.gz \
  && tar -xvf go1.7.1.linux-amd64.tar.gz \
  && mv go /usr/local \
  && rm -r go1.7.1.linux-amd64.tar.gz

RUN npm i -g create-react-app \
  && npm i -g firebase-tools

ENV PATH=$PATH:/usr/local/go/bin

RUN adduser --disabled-password --gecos '' devbox

USER devbox

RUN mkdir ~/work

WORKDIR /home/devbox/work

RUN meteor --version \
  && heroku version
