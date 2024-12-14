
# RESTful APIs in Spring Boot - Interview Preparation

## **What are RESTful APIs?**
RESTful APIs are web services that adhere to the principles of REST (Representational State Transfer). They allow communication between a client and server over HTTP and are used to perform operations on server-side resources.

### **Key Concepts of RESTful APIs**
1. **Resources**:
   - Resources are identified by a **URI (Uniform Resource Identifier)**, e.g., `https://api.example.com/users/123`.

2. **Statelessness**:
   - Each request must contain all the information required for processing.
   - The server does not store session data between requests.

3. **Standard HTTP Methods**:
   - **GET**: Retrieve resources.
   - **POST**: Create resources.
   - **PUT**: Update resources.
   - **PATCH**: Partially update resources.
   - **DELETE**: Remove resources.

4. **HTTP Status Codes**:
   - `200 OK`: Success.
   - `201 Created`: Resource created.
   - `400 Bad Request`: Client error.
   - `401 Unauthorized`: Authentication required.
   - `404 Not Found`: Resource not found.
   - `500 Internal Server Error`: Server error.

5. **Uniform Interface**:
   - Standardized request and response structure using formats like JSON or XML.

6. **Layered Architecture**:
   - The system may use intermediaries like caching layers or proxies.

7. **Cacheability**:
   - Responses can be marked as cacheable to improve performance.

8. **Code on Demand (optional)**:
   - Servers can deliver executable code (e.g., JavaScript) to clients.

---

## **Advantages of RESTful APIs**
- **Scalability**: Stateless design enables scaling.
- **Flexibility**: Decouples client and server.
- **Interoperability**: Supports various platforms (web, mobile, IoT).
- **Reusability**: Endpoints can be reused across multiple applications.
- **Standardization**: Easy to understand due to standardized HTTP methods and status codes.

---

## **RESTful API Example**

### **Base URL**
```
https://api.example.com
```

### **Endpoints**
| HTTP Method | Endpoint             | Description                  | Example Response                  |
|-------------|----------------------|------------------------------|------------------------------------|
| **GET**     | `/users`             | Retrieve all users.          | `[{"id": 1, "name": "John"}]`     |
| **GET**     | `/users/{id}`        | Retrieve a specific user.    | `{"id": 1, "name": "John"}`       |
| **POST**    | `/users`             | Create a new user.           | `{"id": 2, "name": "Jane"}`       |
| **PUT**     | `/users/{id}`        | Update a user completely.    | `{"id": 1, "name": "Updated"}`    |
| **PATCH**   | `/users/{id}`        | Partially update a user.     | `{"id": 1, "email": "new@example.com"}` |
| **DELETE**  | `/users/{id}`        | Delete a user.               | `204 No Content`                  |

---

## **Common RESTful API Questions and Answers**

### **Basic Questions**
1. **What is a RESTful API?**
   - A web service that uses REST principles to allow interaction between a client and server over HTTP.

2. **What are HTTP methods in REST?**
   - GET, POST, PUT, PATCH, DELETE.

3. **What is the difference between PUT and PATCH?**
   - **PUT** replaces the entire resource, while **PATCH** updates only parts of a resource.

4. **What is statelessness in REST?**
   - Each request from a client to the server must contain all the information needed for processing. The server does not store session state.

5. **What are the common HTTP status codes?**
   - `200 OK`: Success.
   - `201 Created`: Resource created.
   - `400 Bad Request`: Client error.
   - `404 Not Found`: Resource not found.

---

### **Advanced Questions**
1. **How do you handle exceptions in a REST API?**
   - Use `@ControllerAdvice` and `@ExceptionHandler` to define global exception handling in Spring Boot.

2. **How do you secure RESTful APIs?**
   - Use **Spring Security** with JWT (JSON Web Tokens) or OAuth2 for authentication and authorization.

3. **What is HATEOAS?**
   - **HATEOAS (Hypermedia as the Engine of Application State)**: It enriches responses with links to related resources to make APIs self-descriptive.

4. **What is the difference between `@Controller` and `@RestController`?**
   - `@Controller` is used for view rendering (e.g., JSP or Thymeleaf). 
   - `@RestController` is used to build RESTful APIs and directly returns data as JSON or XML.

5. **How do you validate incoming requests?**
   - Use `@Valid` and annotations like `@NotNull`, `@Size`, and `@Email` from the `javax.validation` package.

6. **What is the difference between RESTful APIs and SOAP APIs?**
   - REST is lightweight, uses JSON or XML, and follows HTTP methods.
   - SOAP is heavyweight, uses XML, and has strict standards.

7. **How do you handle pagination in REST APIs?**
   - Use Spring Data JPA’s `Pageable` or include query parameters like `?page=1&size=10`.

8. **What is the role of `@RequestBody` and `@ResponseBody` in Spring Boot?**
   - `@RequestBody`: Maps the HTTP request body to a POJO.
   - `@ResponseBody`: Maps the return value of a method to the HTTP response body.

---

## **Best Practices for RESTful APIs**
1. Use proper HTTP status codes to indicate the result of requests.
2. Validate input data to avoid processing invalid requests.
3. Enable CORS if APIs are accessed from different domains.
4. Use pagination for endpoints that return large datasets.
5. Provide detailed error messages for better debugging.
6. Document APIs using Swagger/OpenAPI.

---

This guide should help you confidently tackle RESTful API-related questions in interviews!

