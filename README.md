```sh
go mod init go-grpc
go mod tidy
go get -u google.golang.org/grpc

# go get -u github.com/golang/protobuf/protoc-gen-go
# go get -d google.golang.org/protobuf/protoc-gen-go
# go get -d google.golang.org/protobuf/cmd/protoc-gen-go

go get -u github.com/golang/protobuf/{proto,protoc-gen-go}

export PATH=$PATH:$HOME/go/bin
export PATH=$PATH:/usr/local/go/bin

protoc greet/greetpb/greet.proto --go_out=plugins=grpc:.
```# Go-Proto
