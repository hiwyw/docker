FROM alpine:3.13.5 as build
WORKDIR /home
RUN apk add --update -t deps curl \
    && curl -L https://github.com/xtaci/kcptun/releases/download/v20210103/kcptun-linux-amd64-20210103.tar.gz -o kcptun-linux-amd64-20210103.tar.gz \
    && tar -xvf kcptun-linux-amd64-20210103.tar.gz

FROM alpine:3.13.5
COPY --from=build /home/server_linux_amd64 /usr/local/bin/kcptun-server
ENTRYPOINT ["/usr/local/bin/kcptun-server"] 
CMD ["-c", "/etc/kcptun-server.json"]
