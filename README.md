## Description

This is an example on how to use docker rollout ([https://github.com/wowu/docker-rollout](https://github.com/wowu/docker-rollout)) for a simple rolling deployment with Docker, vanilla NGINX and [nginx/docker-gen](https://github.com/nginx-proxy/docker-gen).

I didn't want to write my NGINX config in docker labels ([nginx-proxy](https://github.com/nginx-proxy/nginx-proxy)), I wanted to keep using the flexibility of nginx.conf files.

And mounting the docker socket in a separate container (not the nginx webserver) is more secure compared to mounting it in the NGINX docker container.

## How to use

1. Install Docker rollout: https://github.com/wowu/docker-rollout#installation
2. Start the webapp containers: `docker rollout -f docker-compose.yml webapp`
3. Launch all the stack: `docker compose up -d`

## How to trigger a redeployment of the webapp

```
docker rollout -f docker-compose.yml webapp
```