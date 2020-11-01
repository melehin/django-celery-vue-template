# Description
This repo contains a template for docker-compose with Django + Postgres + Celery + Redis + Vue.js + Nginx + Caddy (optional)
# Requirements
- docker
- docker-compose
# How to run
Copy __.env.example__ to __.env__ and change it.
> :warning: Only __/api/__ and __/admin/__ routes are proxied to django!


First time run cmd below to start db and wait for a while for db initialization to complete.
```sh
docker-compose -f docker-compose.base.yaml up -d db
```

### Production
```sh
docker-compose -f docker-compose.base.yaml -f docker-compose.prod.yaml up -d
```
### Production with HTTPS (with Let's Encrypt by Caddy)
> Change HTTPS_DOMAIN environment variable inside __.env__ from localhost to your domain name
```sh
docker-compose -f docker-compose.base.yaml -f docker-compose.prod+ssl.yaml up -d
```
### Development (a hot-reload of Vue.js and Django apps. Celery tasks updated by manual required)
```sh
docker-compose -f docker-compose.base.yaml -f docker-compose.dev.yaml up -d
```