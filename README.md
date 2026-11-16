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

## Deploy to Kubernetes

Replace `your-dockerhub-username` in
[`kubernetes/deployment.yaml`](./kubernetes/deployment.yaml) with the Docker Hub
username used to publish the `hello-spring` image, then apply the manifest:

```bash
kubectl apply -f kubernetes/deployment.yaml
kubectl rollout status deployment/hello-spring
kubectl port-forward service/hello-spring 8080:80
```

The app is then available at `http://localhost:8080/api/hello`.
# spring-boot-project
