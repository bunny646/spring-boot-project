# Hello Spring Boot

A small Spring Boot application with one greeting endpoint.

## Run

Requires Java 17 or newer and Maven.

```bash
mvn spring-boot:run
```

Then open `http://localhost:8080/api/hello`. To customize the greeting, use
`http://localhost:8080/api/hello?name=Sam`.

Run the tests with:

```bash
mvn test
```
