FROM denver/xenial-elixir:latest

RUN set -xe \
    && apt update \
    && apt-get -y install curl build-essential git \
    && curl -sL https://deb.nodesource.com/setup_12.x | bash - \
    && apt-get install -y nodejs

