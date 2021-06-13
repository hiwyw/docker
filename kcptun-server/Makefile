VERSION=v1.2.0

docker: build-image
	docker push hiwenzi/kcptun-server:${VERSION}
	docker image prune -f

build-image:
	docker build -t hiwenzi/kcptun-server:${VERSION} --no-cache .
