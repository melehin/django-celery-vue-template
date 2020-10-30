# Description
This repo contains a template for docker-compose with Django + Postgres + Celery + Redis + Vue.js + Nginx
# Requirements
- docker
- docker-compose
# How to run
Copy __.env.example__ to __.env__ and change it.

### Production
```sh
docker-compose --env-file .env -f docker-compose.base.yaml -f docker-compose.prod.yaml up -d
```
### Development (a hot-reload of Vue.js and Django apps. Celery tasks updated by manual required)
```sh
docker-compose --env-file .env -f docker-compose.base.yaml -f docker-compose.dev.yaml up -d
```