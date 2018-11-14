build:
	protoc -I. --go_out=plugins=micro:/home/q00148943/go/src/github.com/Microservices-in-Golang/consignment-service/ \
	proto/consignment/consignment.proto
	docker build -t consignment-service .

run:
	docker run -d -p 50051:50051 \
	-e MICRO_SERVER_ADDRESS=:50051 \
	-e MICRO_REGISTRY=mdns consignment-service


