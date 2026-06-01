# 🏭 Inventory Management System — Java

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![JUnit](https://img.shields.io/badge/JUnit5-25A162?style=for-the-badge&logo=junit5&logoColor=white)

> Enterprise-grade inventory management system built with Java 17, demonstrating industry-standard design patterns and layered architecture.
>
> ---
>
> ## 🚀 Features
>
> - **Product Catalog** — Full CRUD for products with categories and suppliers
> - - **Stock Control** — Real-time stock tracking with low-stock alerts
>   - - **Order Processing** — Purchase and sales order workflow with status tracking
>     - - **Reporting** — Generate stock reports, turnover analysis and audit logs
>       - - **Notifications** — Observer pattern triggers alerts on critical stock levels
>         - - **Pluggable Discounts** — Strategy pattern for flexible pricing rules
>          
>           - ---
>
> ## 🎨 Design Patterns Applied
>
> | Pattern | Where Used | Purpose |
> |---------|-----------|---------|
> | **Factory** | `ProductFactory`, `OrderFactory` | Decouple object creation from business logic |
> | **Observer** | `StockAlert` / `NotificationService` | React to stock level changes |
> | **Strategy** | `DiscountStrategy` implementations | Swap pricing rules at runtime |
> | **Repository** | Data access layer | Abstract database operations |
> | **DTO** | Request/Response objects | Separate API layer from domain model |
> | **Builder** | `ReportBuilder` | Construct complex report objects step by step |
>
> ---
>
> ## 🏗️ Project Structure
>
> ```
> src/
> ├── main/java/com/lluisdam/inventory/
> │   ├── config/              # App configuration
> │   ├── controller/          # REST / CLI controllers
> │   ├── dto/                 # Data Transfer Objects
> │   ├── exception/           # Custom exceptions & handlers
> │   ├── factory/             # Factory pattern classes
> │   ├── model/               # Domain entities
> │   │   ├── Product.java
> │   │   ├── Order.java
> │   │   └── Supplier.java
> │   ├── observer/            # Observer pattern interfaces & implementations
> │   ├── repository/          # Data access layer (JDBC / JPA)
> │   ├── service/             # Business logic
> │   └── strategy/            # Discount strategy implementations
> └── test/java/               # Unit & integration tests
> ```
>
> ---
>
> ## 🛠️ Tech Stack
>
> | Layer | Technology |
> |---|---|
> | Language | Java 17 (LTS) |
> | Build Tool | Apache Maven 3.9 |
> | Database | MySQL 8 |
> | ORM | Hibernate / Spring Data JPA |
> | Testing | JUnit 5 + Mockito |
> | Logging | SLF4J + Logback |
> | API Docs | Springdoc OpenAPI |
>
> ---
>
> ## ⚙️ Getting Started
>
> ### Prerequisites
> - JDK 17+
> - - Maven 3.9+
>   - - MySQL 8+
>    
>     - ### Setup
>    
>     - ```bash
>       # Clone the repository
>       git clone https://github.com/LluisDam/inventory-system-java.git
>       cd inventory-system-java
>
>       # Configure database (edit src/main/resources/application.properties)
>       spring.datasource.url=jdbc:mysql://localhost:3306/inventory_db
>       spring.datasource.username=your_user
>       spring.datasource.password=your_password
>
>       # Build and run
>       mvn spring-boot:run
>       ```
>
> ---
>
> ## 🧪 Testing
>
> ```bash
> mvn test
> ```
>
> Covers unit tests for services and repositories, and integration tests using H2 in-memory database.
>
> ---
>
> ## 📐 Design Decisions
>
> **Why Factory Pattern?** Product types (physical, digital, perishable) share a common interface but require different initialization logic. Factory encapsulates this complexity.
>
> **Why Observer Pattern?** Decouples the stock monitoring logic from email/SMS/push notification delivery, making it easy to add new notification channels without modifying core logic.
>
> **Why Strategy Pattern?** Discount rules change frequently (seasonal, VIP, bulk). Strategy lets us swap algorithms at runtime without altering the order processing code.
>
> ---
>
> ## 📄 License
>
> MIT License — feel free to use this project as a reference or starting point.
>
> ---
>
> *Developed by [Lluis Soberats](https://github.com/LluisDam) — Project Manager & Java Developer*
