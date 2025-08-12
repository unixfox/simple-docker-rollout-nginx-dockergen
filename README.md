## How to use

1. Install Docker rollout: https://github.com/wowu/docker-rollout#installation
2. Start the webapp containers: `docker rollout -f docker-compose.yml webapp`
3. Launch all the stack: `docker compose up -d`

## How to trigger a redeployment of the webapp

```
docker rollout -f docker-compose.yml webapp
```