###PRE-REQUISITES
- pq (can install from a variety of sources)
### DOCKER COMPOSE
```shell
docker compose build --build-arg REDOC_THEME_JSON="$(jq -c . example-theme-options.json)" --no-cache --progress=plain
docker compose up
```

### PURE DOCKER
```shell
docker build . -t my-redoc --build-arg REDOC_THEME_JSON="$(jq -c . example-theme-options.json)" --no-cache --progress=plain
docker run -p "8080:80" my-redoc
```

### ONLY REDOC IMAGE
```shell
docker run -p "8080:80" -e REDOC_OPTIONS="theme='$(jq -c . example-theme-options.json)'" redocly/redoc
```

### VIEW

http://localhost:8080/#tag/store
