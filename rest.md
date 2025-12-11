## REST API

### API

Application Programming Interface (API) is a way for different software applications to communicate with each other.

**REST** (Representational State Transfer) is a loose set of rules that has been the common standard for building APIs since 2000s.

**Rules**:

> 1. Stateless
> 2. Client-Server Architecture
> 3. Cacheable
> 4. Uniform Interface
> 5. Layered System
> 6. Code on Demand (optional)

An API that follows these rules is called a RESTful API.

A Rest API organises the resources (data) using URIs (Uniform Resource Identifiers)

### HTTP Methods

1.. **POST**: Send data to the server to create a new resource. 2. **GET**: Retrieve data from the server. 3. **PUT**: Update an existing resource on the server. 4. **DELETE**: Remove a resource from the server.

Server receives the request, processes it, and sends back a response, usually in JSON or XML format. The first line of the response contains a status code indicating the result of the request.

### Status Codes

- **200 OK**: The request was successful.
- **201 Created**: A new resource was successfully created.
- **400 Bad Request**: The server could not understand the request due to invalid syntax.
- **401 Unauthorized**: The client must authenticate itself to get the requested response.
- **403 Forbidden**: The client does not have access rights to the content.
- **404 Not Found**: The server can not find the requested resource.
- **500 Internal Server Error**: The server has encountered a situation it doesn't know how to handle.
- **503 Service Unavailable**: The server is not ready to handle the request, often due to maintenance or overload.

### Idempotency

When an API is idempotent, it means that making the same request multiple times will have the same effect as making it once.

| Method | Idempotent |
| ------ | ---------- |
| POST   | No         |
| GET    | Yes        |
| PUT    | Yes        |
| DELETE | Yes        |

A Rest implementation should be stateless i.e. each request from client to server must contain all the information needed to understand and process the request. The server should not store any session information about the client between requests.

### Important points
- Use nouns to represent resources in URIs, not verbs. For example, use `/users` instead of `/getUsers`.
- If an API returns a list of items, consider implementing pagination to limit the number of items returned in a single response. Use limit and offset query parameters for this purpose. If not specified , return a default number of items (e.g., 20).
- Use filtering, sorting, and searching query parameters to allow clients to customize the data they receive. For example, `/users?age=25&sort=name`.
- Use versioning in your API to manage changes and ensure backward compatibility. Include the version number in the URI, such as `/v1/users`.

Other popular API styles include GraphQL and gRPC.