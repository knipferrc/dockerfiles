FROM ubuntu:latest
MAINTAINER knipferrc <knipferrc@gmail.com>
RUN apt-get update && apt-get install -y curl git wget sudo nano vim man gcc g++
RUN locale-gen en_US.UTF-8
RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash
RUN curl https://install.meteor.com/ | sh
RUN wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh