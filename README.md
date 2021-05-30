# Go_gprc_protocol-gen-go_proto_server_client

Go gprc protocol-gen-go proto server client

Google published the data serialization method called protocol buffers and the gRPC framework that works over RPC, HTTP / 2 and the protocol buffers themselves

Protocol buffers are a platform agnostic data serialization mechanism

Defined a structure of the data, you can simply use one of the compilers to generate the code responsible for doing the serialization / deserialization of the data.

Go 

Install

https://github.com/google/protobuf/releases

[download][unzip]

protoc-3.17.1-....zip

Set Path in System Variables

[!]

go get -u -v google.golang.org/grpc

[!]

go get -u github.com/golang/protobuf/proto


[!]

go get -u github.com/golang/protobuf/protoc-gen-go

[!]

go get -u -v github.com/golang/protobuf/protoc-gen-go

├───main
│       client.go
│       server.go
│
├───makefile
│       makefile
│
└───proto
        toupper.proto
        
[Compile]
protoc -I proto toupper.proto --go_out=plugins=grpc:proto

├───main
│       client.go
│       server.go
│
├───makefile
│       makefile
│
└───proto
        toupper.pb.go
        toupper.proto

[run]

go build main/server.go

[run]

go build main/client.go
