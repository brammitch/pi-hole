## Simple Docker Pi-hole Config

### Setup

1. Clone and create your own `docker-compose.yml` from `docker-compose.example.yml`
2. Edit `docker-compose.yml`, updating `WEBPASSWORD` and other fields as necessary
3. Start the container

### Starting

```sh
docker compose -f docker-compose.yml up -d
```

### Updating

```sh
docker pull pihole/pihole
```

```sh
# Replace "rsi" with container_name from docker-compose.yml
id=$(docker inspect --format="{{.Id}}" rsi)
```

```sh
docker rm -f $id
```

```sh
docker compose -f docker-compose.yml up -d
```
