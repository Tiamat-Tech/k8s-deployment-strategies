.PHONY: all build test-all test lint vet

all: test-all build

build:
	docker build --no-cache -t containersol/k8s-deployment-strategies .

test-all: vet lint test

test:
	go test -v -parallel=4 ./...

lint:
	golangci-lint run

vet:
	go vet ./...
