FROM composer:2.6.2 AS builder
WORKDIR /build
COPY . .
RUN \
  composer install && \
  rm composer.json composer.lock


FROM php:8.2-apache
RUN \
  docker-php-ext-install mysqli && \
  docker-php-ext-enable mysqli && \
  apt-get update && \
  apt-get upgrade -y
COPY --from=builder /build /var/www/html
