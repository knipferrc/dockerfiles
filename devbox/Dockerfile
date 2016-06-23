FROM ubuntu:latest
MAINTAINER knipferrc <knipferrc@gmail.com>
RUN apt-get update && apt-get install -y curl git wget zsh
RUN rm -rf /var/lib/apt/lists/*
RUN locale-gen en_US.UTF-8
RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash
RUN curl https://install.meteor.com/ | sh