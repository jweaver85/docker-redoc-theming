
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

### VIEW

http://localhost:8080/#tag/store
