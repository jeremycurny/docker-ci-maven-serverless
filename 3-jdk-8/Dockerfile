FROM maven:3-jdk-8

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

ENV FORCE_FULL_BUILD 20200315

RUN \
  curl -sL https://deb.nodesource.com/setup_10.x | bash \
  && apt-get install -y nodejs \
  && apt-get clean autoclean autoremove -y \
  && rm -rf /var/lib/apt/lists/*

RUN \
  npm install -g serverless

RUN \
  curl -sL -o /usr/bin/jq https://github.com/stedolan/jq/releases/download/jq-1.6/jq-linux64 \
  && chmod +x /usr/bin/jq
