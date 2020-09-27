# pre-build stage
FROM ruby:2.7.1-alpine

ENV BUNDLER_VERSION=2.1.2
ENV BUNDLE_PATH="/gems"

COPY .env.example .env

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
  && mkdir -p /var/app \
  && gem install bundler


RUN bundle install
RUN yarn install



