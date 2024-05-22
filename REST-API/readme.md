# Interview Preparation on REST API.

## Index
- [Interview Preparation on REST API.](#interview-preparation-on-rest-api)
  - [Index](#index)
  - [🚀 Topics covered from miscellaneous sources](#-topics-covered-from-miscellaneous-sources)
    - [🍂 What is API?](#-what-is-api)
    - [🍂 What is REST API?](#-what-is-rest-api)
    - [🍂 What does it mean when an API is RESTful?](#-what-does-it-mean-when-an-api-is-restful)
    - [🍂 Difference between traditional API and RESTful API.](#-difference-between-traditional-api-and-restful-api)
    - [🍂 What are the methods used in REST?](#-what-are-the-methods-used-in-rest)
    - [🍂 What is the difference between PUT and PATCH?](#-what-is-the-difference-between-put-and-patch)
    - [🍂 What is a resource in REST?](#-what-is-a-resource-in-rest)
    - [🍂 What is an API endpoint?](#-what-is-an-api-endpoint)
    - [🍂 What is the purpose of HTTP status code?](#-what-is-the-purpose-of-http-status-code)
    - [🍂 What is CORS?](#-what-is-cors)
    - [🍂 Difference between SOAP, gRPC and RESTful API.](#-difference-between-soap-grpc-and-restful-api)
    - [🍂 What are common authentication methods used in RESTful API?](#-what-are-common-authentication-methods-used-in-restful-api)
    - [🍂 How do you handle errors in RESTful API?](#-how-do-you-handle-errors-in-restful-api)
    - [🍂 How do you document RESTful API?](#-how-do-you-document-restful-api)
    - [🍂 What are tools or frameworks commonly used for building RESTful APIs?](#-what-are-tools-or-frameworks-commonly-used-for-building-restful-apis)

<br><br>

## 🚀 Topics covered from miscellaneous sources

### 🍂 What is API?
An API (Application Programming Interface) is a set of rules and protocols that allows one software application to communicate with another. It defines the methods and data formats that applications can use to request and exchange information. APIs are used to enable integration between different software systems, such as web applications, mobile apps, and databases.

<br><br>

### 🍂 What is REST API?
A REST (Representational State Transfer) API (Application Programming Interface) is a type of web service that uses the HTTP protocol to transfer data between clients and servers. REST API is an architectural style that uses standard HTTP methods, such as GET, POST, PUT, DELETE, and PATCH, to perform operations on resources.

<br><br>

### 🍂 What does it mean when an API is RESTful?
When an API is RESTful, it means that the API **follows the principles of REST**.
The key principles of REST are:
- **Client-Server Architecture**: The client and server are separate entities that communicate through a uniform interface.
- **Statelessness**: Each request from the client to the server must contain all the information needed to process the request.
- **Cacheability**: Responses from the server can be cached to improve performance.
- **Uniform Interface**: The API should have a uniform interface that is easy to understand and use.
- **Layered System**: The API can be layered to improve scalability and security.
- **Code on Demand (optional)**: The server can send executable code to the client to extend functionality.

<br><br>

### 🍂 Difference between traditional API and RESTful API.
| Traditional API | RESTful API |
| --- | --- |
| Uses custom protocols and data formats | Uses standard protocols (HTTP) and data formats (JSON, XML) |
| Can be more complex and rigid | Is simpler and more flexible |
| May not be easily scalable or maintainable | Is designed for scalability and maintainability |
| May not be easily understood by developers | Is easy to understand and use |
| May not be easily integrated with other systems | Is designed for integration with other systems |

<br><br>

### 🍂 What are the methods used in REST?
The methods used in REST are:
- GET: Used to retrieve data from a server.
- POST: Used to send data to a server to create a new resource.
- PUT: Used to update an existing resource on a server.
- DELETE: Used to delete a resource from a server.
- PATCH: Used to update a part of an existing resource on a server.

<br><br>

### 🍂 What is the difference between PUT and PATCH?
The main difference between PUT and PATCH is that PUT is used to **update an entire resource**, while PATCH is used to **update a part of a resource**. When using PUT, the client sends the entire resource to the server, which replaces the existing resource with the new one. When using PATCH, the client sends only the part of the resource that needs to be updated, and the server updates that part of the resource.

<br><br>

### 🍂 What is a resource in REST?
A resource in REST is an object or piece of data that can be accessed by a client through a unique URI (Uniform Resource Identifier). Resources can be anything that can be represented in a digital form, such as a user, a product, or an order. It is similar to an object in object-oriented programming.

<br><br>

### 🍂 What is an API endpoint?
An API endpoint is a specific URL that represents a resource in a REST API. It is the location where clients can access or interact with the resource. Each endpoint is associated with one or more HTTP methods, such as GET, POST, PUT, DELETE, and PATCH, which define the operations that can be performed on the resource.

<br><br>

### 🍂 What is the purpose of HTTP status code?
The purpose of HTTP status codes is to indicate the outcome of an HTTP request. They provide information about the status of the request, such as whether it was successful, failed, or redirected. Status codes are divided into different categories, such as 1xx (Informational), 2xx (Success), 3xx (Redirection), 4xx (Client Error), and 5xx (Server Error).

<br><br>

### 🍂 What is CORS?
CORS (Cross-Origin Resource Sharing) is a security feature implemented by web browsers to prevent unauthorized access to resources on a different origin (domain). It allows servers to specify which origins are allowed to access their resources by adding the appropriate CORS headers to the HTTP response. This helps prevent cross-site request forgery (CSRF) attacks.

<br><br>

### 🍂 Difference between SOAP, gRPC and RESTful API.
| Feature | SOAP | gRPC | RESTful API |
| --- | --- | --- | --- |
| Protocol | Uses XML-based protocol | Uses Protocol Buffers (protobuf) | Uses HTTP protocol |
| Data Format | Uses XML | Uses binary format | Uses JSON, XML, or other data formats |
| Performance | Can be slower due to XML parsing | Faster due to binary serialization | Depends on implementation |
| Error Handling | Has built-in error handling | Has built-in error handling | Uses HTTP status codes for error handling |
| Language Support | Supports multiple languages | Supports multiple languages | Supports multiple languages |
| Complexity | Can be more complex | Can be less complex | Can be less complex |
| Security | Supports WS-Security for encryption and authentication | Supports TLS for encryption and authentication | Supports various authentication methods |
| Scalability | Can be less scalable | Can be more scalable | Can be scalable |
| Statelessness | Can be stateful | Can be stateful | Is stateless |
| Usage | Used in enterprise applications  | Used in microservices and cloud-native applications | Used in web applications and APIs |

**Enterprise application**: An enterprise application is a large software system that is used by organizations to manage their business processes and operations. It typically consists of multiple modules or components that work together to support various functions, such as accounting, human resources, and customer relationship management.

<br><br>

### 🍂 What are common authentication methods used in RESTful API?
The common authentication methods used in RESTful API are:
- Basic Authentication: Uses a username and password for authentication.
- Token-based Authentication: Uses a token (such as JWT) for authentication.
- OAuth: Uses OAuth 2.0 protocol for authentication and authorization.
- API Key: Uses an API key for authentication. (e.g., Google Maps API)

<br><br>

### 🍂 How do you handle errors in RESTful API?
Errors in RESTful API are typically handled by returning appropriate HTTP status codes along with error messages in the response body. Some common HTTP status codes used for error handling are:
- 400 Bad Request: The request is invalid or malformed.
- 401 Unauthorized: The request requires user authentication.
- 403 Forbidden: The server refuses to process the request.
- 404 Not Found: The requested resource is not found.
- 500 Internal Server Error: The server encountered an unexpected condition.
- 503 Service Unavailable: The server is temporarily unavailable.
- 504 Gateway Timeout: The server did not receive a timely response from an upstream server.

<br><br>

### 🍂 How do you document RESTful API?
RESTful API can be documented using tools such as Swagger, OpenAPI, or Postman. These tools allow us to define the API endpoints, request and response formats, authentication methods, and other details in a structured way. The documentation can be generated in various formats, such as HTML, PDF, or JSON, and can be shared with developers and clients.

<br><br>

### 🍂 What are tools or frameworks commonly used for building RESTful APIs?
Some common tools or frameworks used for building RESTful APIs are:
- Express.js: A Node.js web application framework.
- Spring Boot: A Java-based framework for building web applications.
- Django: A Python-based web framework.
- Flask: A Python-based microframework.
- Ruby on Rails: A Ruby-based web application framework.
- ASP.NET Web API: A framework for building web APIs using .NET.
- Laravel: A PHP-based web application framework.

<hr>