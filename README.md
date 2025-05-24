# Java Spring Boot Microservices App 🚀

**Java Spring Boot Microservices App** is a production-ready backend system built using Spring Boot and cloud-native technologies. It consists of multiple modular microservices communicating via gRPC and Kafka, secured through JWT authentication, and orchestrated through Docker and an API Gateway.

---

## ✨ Features

- 🏥 **Patient Service**: REST APIs to manage patient data with full validation and OpenAPI documentation.
- 💰 **Billing Service**: gRPC-based billing account creation integrated with patient registration flow.
- 📊 **Analytics Service**: Kafka consumer that processes patient events for real-time insights.
- 🔐 **Auth Service**: Handles user login, password encryption, JWT generation, and token validation.
- 🌐 **API Gateway**: Central routing layer with JWT filter, path rewriting, and Swagger aggregation.
- ☁️ **Infrastructure-as-Code**: Automated AWS deployment using CloudFormation and LocalStack for local testing.

---

## 🛠️ Tech Stack

- **Java 21**, **Spring Boot 3.5**
- **Spring Cloud Gateway**
- **gRPC** (Protocol Buffers)
- **Apache Kafka**
- **Spring Security + JWT**
- **Docker & Docker Compose**
- **OpenAPI (Swagger)**
- **AWS CloudFormation**, **LocalStack**

---

## 📁 Microservices Breakdown

| Service            | Description                                                        |
|--------------------|--------------------------------------------------------------------|
| `patient-service`   | Exposes REST APIs for CRUD operations on patient data. Emits events to Kafka. |
| `billing-service`   | Exposes a gRPC method `CreateBillingAccount` triggered by patient creation. |
| `analytics-service` | Kafka consumer that listens to patient-related events.            |
| `auth-service`      | Provides secure login, token generation, and JWT validation.     |
| `api-gateway`       | Routes external traffic and applies security/exception filters.  |

---

## 🎯 Future Enhancements

- Integrate distributed tracing with Zipkin or Jaeger.
- Add service discovery with Spring Cloud Eureka.
- Auto-scaling setup on AWS ECS Fargate.
- Implement centralized logging with ELK or Loki.

---

## 📈 Key Highlights

- 📡 High-performance service-to-service communication via gRPC  
- 🔒 Fully stateless JWT-based security  
- ⚙️ Event-driven architecture using Kafka  
- 📄 API documentation via OpenAPI for all services  
- 🚢 Easily portable and deployable using Docker & IaC  

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).
