# abh-task

Docker containerized microservices demo.

## Prerequisites

- Docker
- Docker Compose

## Starting the app

```
docker-compose up
```

If re-building after a change:

```
docker-compose up --build
```

## Stopping the app

```
docker-compose down
```

Additionally, if you want to stop the app and remove the volume:

```
docker-compose down -v
```

## Accessing the app

**Node app:**

- `http://localhost:8081/node/api/v1/result`

**Spring app:**

- Node check: `http://localhost:8080/java/api/v1/node`
- DB check: `http://localhost:8080/java/api/v1/status`

## Checking the app

After running `docker-compose up`, open another terminal and execute:

```
bash <(curl -s https://raw.githubusercontent.com/kkenan/basic-microservices/master/health_check.sh)
```

If successful, you should see "All checks passed. Congrats!"
