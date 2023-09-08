# Docker Image

## Get Startted

```shell
docker run --rm \
  --interactive --tty \
  --publish 40080:80 \
  --mount type=bind,source="${PWD}/.env",target=/var/www/html/.env \
  landing
```

## Open browser

Open browser http://127.0.0.1:40080/web/

## Build

```shell
docker build \
  -t landing \
  -f docker/Dockerfile \
  .
```
