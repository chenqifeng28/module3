export tag=v1.0
root:
	export ROOT=github.com/chenqifeng28/module3

build:
	echo "building httpserver binary"
	mkdir -p bin/amd64
	CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o bin/amd64 .

release: build
	echo "building httpserver container"
	docker build -t chenqf28/httpserver:${tag} .

#push: release
#	echo "pushing chenqf28/httpserver"
#	docker push chenqf28/httpserver:v1.0
