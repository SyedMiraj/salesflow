<div align="center">
  <h1 style="color: #2c3e50;">SalesFlow</h1>
  <p style="color: #7f8c8d;">A Comprehensive Sales Management System</p>
</div>

---

## 🌟 Key Features

SalesFlow is designed to streamline your sales operations, providing a robust platform to manage everything from suppliers to customers. Here's what makes SalesFlow stand out:

* **User-Friendly Interface:** An intuitive design ensures a smooth experience for all users.
* **Comprehensive Modules:** Covers all essential aspects of sales management.
* **Customizable Reports:** Generate detailed reports to gain valuable insights.
* **Secure Authentication:** JWT-based authentication for enhanced security.


---

## 🏗️ Architecture Features

SalesFlow is built using a modern microservices architecture with the following technologies:

* Spring Boot + Spring Cloud microservices
* PostgreSQL DB
* Kafka for logging and order events
* Docker & Kubernetes for deployment
* AWS S3 for persistence
* GitHub Actions for CI/CD
* Next.js (React) frontend with clean UI per module

---

## 📦 Key Modules

SalesFlow is organized into several key modules, each designed to handle a specific aspect of sales management:

1.  **Auth Service**
    * Handles login, JWT-based authentication, and user roles (ADMIN, SALES\_REP)
    * Registers users and issues secure tokens
    * <span style="color: #3498db;">Key Functionality:</span> Securely manage users and their permissions.
    * <span style="color: #3498db;">Github:</span> https://github.com/SyedMiraj/salesflow-auth-service

2.  **Product & Supplier Service**
    * Manages product catalog
    * Tracks stock levels (inventory)
    * Maintains supplier information
    * <span style="color: #3498db;">Key Functionality:</span> Efficiently manage supplier information and track purchases.
    * <span style="color: #3498db;">Github:</span> https://github.com/SyedMiraj/salesflow-inventory-service

3.  **Sales Service**
    * Handles sales orders and cart management
    * Manages customer details
    * Tracks payments and invoices
    * Updates product inventory after sales
    * <span style="color: #3498db;">Key Functionality:</span> Manage sales orders from creation to delivery.
    * <span style="color: #3498db;">Github:</span> https://github.com/SyedMiraj/salesflow-sales-service

4.  **Report Service**
    * Generates reports: sales summary, daily sales, inventory levels, customer payments, etc.
    * <span style="color: #3498db;">Key Functionality:</span> Get a bird's-eye view of your sales performance with insightful reports.
    * <span style="color: #3498db;">Github:</span> https://github.com/SyedMiraj/salesflow-report-service

5.  **Gateway Service (Spring Cloud Gateway)**
    * Entry point for frontend (Next.js)
    * Routes requests to backend services
    * Handles authentication and authorization with JWT filter
    * <span style="color: #3498db;">Key Functionality:</span> Acts as a single entry point for the application, handling routing and security.
    * <span style="color: #3498db;">Github:</span> https://github.com/SyedMiraj/salesflow-gateway-service

---

## 🧭 System Architecture Diagram

```mermaid
graph TD;
  Frontend[Next.js] --> Gateway[Spring Cloud Gateway]
  Gateway --> AuthService
  Gateway --> InventoryService
  Gateway --> SalesService
  Gateway --> ReportService
```

---

## 🛠️ Deployment Lifecycle

This diagram illustrates the complete flow of the Sales Management System from development to deployment using Docker and Kubernetes on AWS EC2. The system includes microservices, CI/CD pipeline, and PostgreSQL running in a container within the Kubernetes cluster.

```mermaid
graph LR
  subgraph Dev["🧑‍💻 Development"]
    A1[Write Code in Microservices: Spring Boot, Next.js]
    A2[Use Common Module for Shared DTOs/Utils]
    A3[Commit Code to GitHub Repo]
  end

  subgraph CI["⚙️ CI with GitHub Actions"]
    B1[Run Unit Tests]
    B2[Build JARs and Docker Images]
    B3[Push Images to Docker Hub or ECR]
  end

  subgraph CD["🚀 CD with Kubernetes"]
    C1[Connect to AWS EC2-based K8s Cluster]
    C2[Apply Kubernetes YAMLs]
    C3[Create Deployments, Services, Ingress]
    C4[Load Balancer Exposes Gateway Service]
  end

  subgraph Ops["🧩 System Running on K8s"]
    D1[Auth Service Pod]
    D2[Inventory Service Pod]
    D3[Sales Service Pod]
    D4[Report Service Pod]
    D5[Gateway Service Pod]
    D6[(PostgreSQL DB Pod)]
  end

  subgraph FE["🖥️ Frontend"]
    E1[Next.js App Connects to Gateway via HTTPS]
  end

  %% Flows
  A1 --> A2 --> A3 --> B1 --> B2 --> B3 --> C1 --> C2 --> C3 --> C4
  C4 --> E1
  C3 --> D1
  C3 --> D2
  C3 --> D3
  C3 --> D4
  C3 --> D5
  D1 --> D6
  D2 --> D6
  D3 --> D6
  D4 --> D6
```

---

## 📄 License

[MIT](LICENSE)

---

## 📞 Contact

For any questions or support, please contact us at [smiraj2507@gmail.com](mailto:smiraj2507@gmail).

---

<div align="center">
  <p style="color: #95a5a6;">Thank you for using SalesFlow!</p>
</div>
