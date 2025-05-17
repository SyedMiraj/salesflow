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
* AWS RDS + S3 for persistence
* GitHub Actions for CI/CD
* Next.js (React) frontend with clean UI per module

---

## 📦 Key Modules

SalesFlow is organized into several key modules, each designed to handle a specific aspect of sales management:

1.  **User Management**
    * Roles: Admin, Sales Representative
    * Authentication & authorization (JWT)
    * Audit tracking of user actions
    * <span style="color: #3498db;">Key Functionality:</span> Securely manage users and their permissions.

2.  **Supplier Management**
    * Manage supplier profiles
    * Track purchases from suppliers
    * View purchase history
    * <span style="color: #3498db;">Key Functionality:</span> Efficiently manage supplier information and track purchases.

3.  **Product & Inventory Management**
    * CRUD for products with SKU, price, stock
    * Inventory tracking (stock in/out)
    * Low stock alerts
    * <span style="color: #3498db;">Key Functionality:</span> Keep a close eye on your inventory and product details.

4.  **Sales Order Management**
    * Create & manage customer orders
    * Real-time stock check
    * Order status: Pending, Confirmed, Delivered
    * <span style="color: #3498db;">Key Functionality:</span> Manage sales orders from creation to delivery.

5.  **Customer Management**
    * Manage customer profiles
    * Track sales history per customer
    * <span style="color: #3498db;">Key Functionality:</span> Maintain detailed customer profiles and track their purchase history.

6.  **Payment & Invoice Management**
    * Create invoices linked to sales orders
    * Track payments (Cash, Card, Bank)
    * View payment status: Paid, Unpaid, Partial
    * <span style="color: #3498db;">Key Functionality:</span> Handle invoicing and payment tracking with ease.

7.  **Dashboard & Reports**
    * Daily/Monthly sales overview
    * Best-selling products
    * Payments due
    * Inventory status
    * <span style="color: #3498db;">Key Functionality:</span> Get a bird's-eye view of your sales performance with insightful reports.

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
