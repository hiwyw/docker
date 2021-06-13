VERSION=v1.2.0
SHADOWSOCKS_VERSION=v1.11.1

docker: build-image
	docker push hiwenzi/shadowsocks-server:${VERSION}
	docker image prune -f

build-image:
	docker build -t hiwenzi/shadowsocks-server:${VERSION} --build-arg ss_version=${SHADOWSOCKS_VERSION} --no-cache .
