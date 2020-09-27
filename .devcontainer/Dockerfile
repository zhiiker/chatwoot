# pre-build stage
ARG VARIANT=2.7
FROM mcr.microsoft.com/vscode/devcontainers/ruby:${VARIANT}

ARG NODE_VERSION="lts/*"
RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && nvm install ${NODE_VERSION} 2>&1"

RUN apt-get update \
  && apt-get -y install --no-install-recommends \
    libssl-dev \
    tar \
    tzdata \
    postgresql-client \
    yarn \
    git \
    imagemagick \
    zsh

# packages: postgresql-server-dev-all

RUN gem install bundler

# [Optional] Uncomment this line to install global node packages.
# RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && npm install -g <your-package-here>" 2>&1



