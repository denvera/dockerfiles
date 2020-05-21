FROM ubuntu:focal
ENV DEBIAN_FRONTEND=noninteractive
RUN set -xe \
    && apt update \
    && apt-get -y install wget build-essential git locales \
    && wget https://packages.erlang-solutions.com/erlang-solutions_2.0_all.deb \
    && dpkg -i erlang-solutions_2.0_all.deb


RUN set -xe \
    && export LANG=en_US.UTF-8 \
    && echo $LANG UTF-8 > /etc/locale.gen \
    && locale-gen \
    && update-locale LANG=$LANG

RUN set -xe \
    && apt-get -y update \
    && apt-get -y install esl-erlang \
    && apt-get -y install elixir

ENV LANG=en_US.UTF-8
CMD ["iex"]
