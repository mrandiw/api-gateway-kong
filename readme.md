# kong-go-plugin-sample

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/made-with-go.svg)](https://forthebadge.com)

Feature :

1. Authentication and Authorization
2. Service Discovery

```
docker build -t kong-demo .
```

Images are built and we can run them as containers.

```
docker run -ti --rm --name kong-go-plugins \
  -e "KONG_DATABASE=off" \
  -e "KONG_GO_PLUGINS_DIR=/tmp/go-plugins" \
  -e "KONG_DECLARATIVE_CONFIG=/tmp/config.yml" \
  -e "KONG_PLUGINS=key-checker" \
  -e "KONG_PROXY_LISTEN=0.0.0.0:8080" \
  -p 8080:8080 \
  kong-demo
```
