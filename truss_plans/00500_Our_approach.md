
# Our approach (first draft)

- A single definition of the service contract / API
	- Protobuf definition
	- This will require HTTP/JSON endpoint annotations
- Documentation which can be generated from the definition file
	- From the comments of the protobuf definition
- Automatic generation of all scaffolding for `go-kit`
