# REST, gRPC and GraphQL

This project is an attempt to gather the foundations of three common API Styles –REST, gRPC and GraphQL. It also works as a guide on how each one of these styles tackles some everyday usage cases.

## Demo project
See [implementation project](src/)

## Project description
1. [Introduction](docs/apis_introduction.md)
2. [REST](docs/rest.md)
3. [GraphQL](docs/graphql.md)
4. [gRPC](docs/grpc.md)

### Comparison table

| Usage                              | REST                                                                      | GraphQL                                       | gRPC                                                          |
|------------------------------------|---------------------------------------------------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| [Contract][]                       | HATEOAS or OpenAPI                                                        | GraphQL Schema Language: operations           | Protocol Buffers: rpc                                         |
| [Schema definition][]              | Resource oriented.<br />HTTP response headers, Media Type and JSON Schema | Graph oriented.<br />GraphQL Schema Language  | Resource and Action oriented.<br />Protocol Buffers: messages |
| [Standard methods][]               | `GET`, `POST`, `PUT`, `PATCH`, `DELETE`                                   | `query` and `mutation`                        | Through rpc operations                                        |
| [Get][]                            | `GET`                                                                     | `query`                                       | `Get` rpc operation                                           |
| [Get (representation)][]           | ✔️ Content Negotiation                                                     | ✘ Only JSON                                   | ✘ only one. Default: Protocol Buffers                         |
| [Get (custom)][]                   | Sparse fieldsets. Embedded resources                                      | Native support                                | `FieldMask`                                                   |
| [List][]                           | `GET`. Custom pagination, sorting and filtering                           | `query`. Standard pagination and sorting      | `List` and `Search` rpc operations                            |
| [Create][]                         | `POST` or `PUT`                                                           | `mutation`                                    | `Create` rpc operation                                        |
| [Update][]                         | `PUT`                                                                     | `mutation`                                    | `Update` rpc operation (unrecommended)                        |
