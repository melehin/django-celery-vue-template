# Description
This repo contains a template for docker-compose with Django + Postgres + Celery + Redis + Vue.js
# Requirements
- docker
- docker-compose
# How to run
Copy __.env.example__ to __.env__ and make changes first.

### Production
```sh
docker-compose --env-file .env -f docker-compose.base.yaml -f docker-compose.prod.yaml up -d
```
### Development
```sh
docker-compose --env-file .env -f docker-compose.base.yaml -f docker-compose.dev.yaml up -d
```