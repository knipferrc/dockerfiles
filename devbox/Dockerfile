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
    build-essential \
    tar

RUN locale-gen en_US.UTF-8

RUN curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -

RUN apt-get install nodejs -y

RUN curl https://install.meteor.com/ | sh

RUN wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh

RUN curl -O https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz

RUN tar -xvf go1.6.2.linux-amd64.tar.gz

RUN mv go /usr/local

ENV PATH=$PATH:/usr/local/go/bin

RUN rm -r go1.6.2.linux-amd64.tar.gz

RUN adduser --disabled-password --gecos '' devbox

USER devbox

WORKDIR /home/devbox
