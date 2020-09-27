# pre-build stage
FROM ruby:2.7.1-alpine

RUN apk update \
  && apk add \
    openssl \
    tar \
    build-base \
    tzdata \
    postgresql-dev \
    postgresql-client \
    nodejs \
    yarn \
    git \
    imagemagick \
  && gem install bundler



