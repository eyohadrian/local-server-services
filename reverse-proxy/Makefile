# Makefile

.PHONY: clean build run start

clean:
	-docker stop reverse-proxy-container
	-docker rm reverse-proxy-container
	-docker rmi reverse-proxy

build:
	docker build -t reverse-proxy .

run: build
	docker run -d -p 80:80 --name reverse-proxy-container --network="host" reverse-proxy

start:
	docker start reverse-proxy-container
