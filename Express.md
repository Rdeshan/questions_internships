1. What is Express.js?

Express.js is a minimal and flexible Node.js web framework used to build web applications and REST APIs.

2. Why use Express instead of Node.js only?

Express simplifies routing, request handling, and middleware management compared to plain Node.js.

3. What is middleware in Express?

Middleware is a function that executes between the request and the response cycle.

4. Types of middleware in Express?

Application-level, Router-level, Built-in, Error-handling, and Third-party middleware.

5. What is app.use()?

app.use() is used to register middleware in an Express application.

6. What is routing in Express?

Routing defines how an application responds to client requests at specific URLs and HTTP methods.

7. What are HTTP methods used in Express?

GET, POST, PUT, PATCH, DELETE.

8. Difference between GET and POST?

GET retrieves data, while POST sends data to the server.

9. What is req and res?

req represents the client request and res represents the server response.

10. What is req.params?

It contains route parameters from the URL.

11. What is req.query?

It contains query string parameters.

12. What is req.body?

It contains data sent from the client, usually in POST or PUT requests.

13. What is express.json()?

It is built-in middleware used to parse JSON request bodies.

14. What is CORS?

CORS (Cross-Origin Resource Sharing) allows or restricts resources requested from another domain.

15. What is REST API?

A REST API is an API that follows REST principles and uses HTTP methods for CRUD operations.

16. How do you handle errors in Express?

Using error-handling middleware with four parameters: (err, req, res, next).

17. What is next() in Express?

next() passes control to the next middleware function.

18. What is Router in Express?

express.Router() is used to create modular and reusable route handlers.

19. How do you connect Express with MongoDB?

By using libraries like Mongoose to connect Express applications to MongoDB.

20. How do you start an Express server?

By calling app.listen(port, callback).
