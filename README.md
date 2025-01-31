# Hawtio Spring Boot Project

Welcome to the **Hawtio Spring Boot Project**! This project integrates the Hawtio management console with a Spring Boot application for monitoring and management.

---

## **Clone the Repository**

Start by cloning the repository to your local machine:

```bash
git clone https://github.com/radlee/hawt_spring_io.git
```

Navigate to the project directory:

```bash
cd hawt_spring_io
```

---

## **Run the Application**

Use Maven to start the Spring Boot application:

```bash
mvn spring-boot:run
```

Alternatively, you can package the application and run the JAR file:

1. Package the application:
   ```bash
   mvn clean package
   ```

2. Run the JAR file:
   ```bash
   java -jar target/hawt_spring_io.jar
   ```

---

## **Access Hawtio**

Once the application starts, the Hawtio management console will be available at:

```
http://localhost:8080/hawtio
```

(Replace `8080` with the port specified in your Spring Boot application if it’s different.)

---

## **Configuration**

### Disable Authentication (Optional)
For development purposes, you can disable authentication by adding the following to `application.properties`:

```properties
hawtio.authenticationEnabled=false
```

### Enable Authentication (Recommended for Production)
Follow the steps to set up secure access as outlined in the project documentation.

---

## **Troubleshooting**

- **Dependency Issues**: Ensure all dependencies are properly installed by running:
  ```bash
  mvn dependency:resolve
  ```

- **Port Conflicts**: If the default port is in use, specify a different port in `application.properties`:
  ```properties
  server.port=8081
  ```

- **"Host Not Allowlisted" Error**: Add the required host to the allowlist in `application.properties`:
  ```properties
  hawtio.proxyAllowlist=localhost,127.0.0.1,glu-engine-bay-36.dev.flash.co.za
  ```

---

## **Contributing**

Contributions are welcome! Please fork the repository and submit a pull request.

---

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.

