# E-commerce-App
A NodeJS App with Microservice Architecture which provides services like order, carts, catalog, user management and a service registry

## Setup env

### Start MongoDB in Docker
Run `docker pull mongo` when doing it the first time followed by `docker run --name mongodb -p 37017:27017 -d mongo`.

### Start Redis in Docker
Run `docker pull redis` followed by `docker run --name redis -p 7379:6379 -d redis`

#### Install and run Redis Commander
Make sure you have installed it with `npm install -g redis-commander` then run `redis-commander --redis-port=7379`.

### Start Jaeger in Docker
```sh
docker run --name jaeger \
  -e COLLECTOR_OTLP_ENABLED=true \
  -p 16686:16686 \
  -p 4317:4317 \
  -p 4318:4318 \
  -d jaegertracing/all-in-one:1.45
```
UI: http://localhost:16686

### Start RabbitMQ in Docker
`docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 -d rabbitmq:3.11-management`

Management interface: http://localhost:15672/ user: guest, password: guest
