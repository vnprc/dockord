### build and start the docker cloud
```
docker compose build --no-cache
docker compose up
```

### start an individual docker insatnce
```
docker run -it dockord_ord bash
```

### hop into a running docker container bash shell
```
docker exec -it dockord-ord-1 bash
```

### create a regtest ord wallet
```
ord -r --cookie-file /bitcoin/.bitcoin/regtest/.cookie --rpc-url http://bitcoind:8332/ wallet
```