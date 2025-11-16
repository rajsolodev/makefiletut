.PHONY: up down start stop

COMPOSE = docker compose -f docker-compose.yml
SERVICE = fastapi_app

up:
	$(COMPOSE) up -d

down:
	$(COMPOSE) down

start:
	$(COMPOSE) start

stop:
	$(COMPOSE) stop

bash:
	$(COMPOSE) exec $(SERVICE) bash

dev:
	uv run fastapi dev