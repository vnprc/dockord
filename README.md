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
ord -r --cookie-file /bitcoin/.bitcoin/regtest/.cookie --rpc-url http://bitcoind:8332/ wallet create
```

### bitcoind health check
```
/bitcoin/.bitcoin/bitcoin-cli --rpcconnect=bitcoind --rpcport=8332 --rpccookiefile=/bitcoin/.bitcoin/regtest/.cookie getblockcount
```


### generate 101 blocks to address
```
/bitcoin/.bitcoin/bitcoin-cli --rpcconnect=bitcoind --rpcport=8332 --rpccookiefile=/bitcoin/.bitcoin/regtest/.cookie generatetoaddress 101 bcrt1paw2gyzatqtccenymqfxfrxx4fn235v3sfxvs7sqe7dlcm0raqwwsp0ul80
```