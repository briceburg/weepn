# weepn


## get dirty

##### generate key and start dsvpn service on local port 4443
```
dd count=1 bs=32 if=/dev/urandom of=vpn.key
DSVPN_KEY="$(base64 < vpn.key)" \
  docker-compose up --build
```


##### test service using the dsvpn client (assuming it's installed)
```
dsvpn client vpn.key 127.0.0.1 4443
```

```
> ...
> Interface: [tun0]
> Trying to reconnect
> Connecting to 127.0.0.1:4443...
> et.ipv4.tcp_congestion_control = bbr
> Connected
```

:boom:
