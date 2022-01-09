FROM ruby:3.1.0

ENV LC_ALL=C.UTF-8

RUN \
  curl -sL https://deb.nodesource.com/setup_16.x | bash - && \
  curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
  curl -sS https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add - && \
  echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main" |  tee /etc/apt/sources.list.d/pgdg.list && \
  apt-get update && \
  apt-get install -y --no-install-recommends \
      postgresql-client-13 \
      sqlite3 \
      nodejs \
      yarn \
      imagemagick \
      mecab libmecab-dev mecab-ipadic-utf8 && \
  rm -rf /var/lib/apt/lists/*  /tmp/*
