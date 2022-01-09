FROM ruby:3.1.0

ENV LC_ALL=C.UTF-8

RUN \
  curl -sS https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add - && \
  echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main" |  tee /etc/apt/sources.list.d/pgdg.list && \
  apt-get update && \
  apt-get install -y --no-install-recommends \
      postgresql-client-13 \
      sqlite3 \
      imagemagick \
      mecab libmecab-dev mecab-ipadic-utf8 && \
  rm -rf /var/lib/apt/lists/*  /tmp/*
