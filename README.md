## Simple Docker Pi-hole Config

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
