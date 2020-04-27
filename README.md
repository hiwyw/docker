# docker
## shadowsocks-server
```
docker run -d --name ssserver --net=host -v $(pwd)/shadowsocks-server.json:/etc/shadowsocks-server.json hiwenzi/shadowsocks-server:v1.0.0
```
## kcptun-server
```
docker run -d --name kcptun-server --net=host -v $(pwd)/kcptun-server.json:/etc/kcptun-server.json hiwenzi/kcptun-server:v1.0.0
```