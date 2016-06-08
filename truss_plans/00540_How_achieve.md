
# How'll we achieve this?

1. A specially annotated Protobuf definition
2. Documentation which can be generated from the definition file
3. Automatic generation of `go-kit` boilerplate (transports, services, middlewares, etc)
4. Generation of (ugly) Swagger spec from this Protobuf definition with `protoc-gen-swagger`

