FROM php:8.2-cli

RUN apt-get update \
  && apt-get install -y --no-install-recommends libpng-dev libzip-dev \
  && docker-php-ext-install -j"$(nproc)" gd zip \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /app