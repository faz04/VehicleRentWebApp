# 🚗 Vehicle Rental Web Application

A production-ready **Java Jakarta EE web application** for managing vehicle rental operations. The system provides secure user registration and authentication, vehicle browsing, online booking with payment slip uploads, administrative management, reviews, notifications, and a complete file-based persistence layer.

---

## 🛠️ Tech Stack

| Layer | Technology |
|--------|------------|
| Backend | Java 23, Jakarta EE |
| Web Framework | Jakarta Servlets 6.1, JSP |
| Frontend | HTML5, CSS3, Tailwind CSS, JavaScript |
| Build Tool | Apache Maven |
| Server | Apache Tomcat 11+ |
| Storage | File-Based Persistence (`WEB-INF` Text Files) |

---

## 📁 Project Structure

```text
src/
├── main/
│   ├── java/com/vehicle/rental/vehiclerentalwebapp/
│   │   ├── controller/          ← Servlet controllers
│   │   ├── model/               ← Java model classes
│   │   ├── service/             ← Business logic
│   │   ├── repository/          ← File handling utilities
│   │   └── util/                ← Helper classes
│   │
│   ├── webapp/
│   │   ├── css/
│   │   ├── images/
│   │   ├── uploads/             ← Payment slip uploads
│   │   ├── WEB-INF/
│   │   │   ├── users.txt
│   │   │   ├── admin.txt
│   │   │   ├── vehicles.txt
│   │   │   ├── bookings.txt
│   │   │   ├── reviews.txt
│   │   │   ├── notifications.txt
│   │   │   └── web.xml
│   │   └── *.jsp                ← JSP pages
│   │
│   └── resources/
└── pom.xml
```

---

## ✨ Features

### 👤 User Features

- User Registration
- Secure Login
- Browse Available Vehicles
- Search & Sort Vehicles
- Vehicle Booking
- Payment Slip Upload (JPEG, Max 5MB)
- Booking History
- Notification Center
- Submit Reviews

### 👨‍💼 Administrator Features

- Secure Admin Login
- Dashboard Overview
- Add New Vehicles
- Update Vehicle Details
- Delete Vehicles
- Approve Bookings
- Reject Bookings
- Manage Users
- Manage Admin Accounts
- Send Notifications

---

## 📋 Application Modules

| Module | Description |
|---------|-------------|
| Authentication | User & Admin Login System |
| Vehicle Management | Add, Edit, Delete Vehicles |
| Booking Management | Rental Reservations |
| Payment Management | Payment Slip Upload |
| Review Management | Customer Reviews |
| Notification System | Admin/User Notifications |
| File Storage | Text File Database |

---

## 📂 Data Storage

The application stores data inside the **WEB-INF** directory using plain text files.

| File | Purpose |
|------|---------|
| `users.txt` | Registered Users |
| `admin.txt` | Administrator Accounts |
| `vehicles.txt` | Vehicle Inventory |
| `bookings.txt` | Rental Bookings |
| `reviews.txt` | Customer Reviews |
| `notifications.txt` | User/Admin Notifications |

> **Note:** These files are empty by default and act as the application's lightweight database.

---

## 🚀 Getting Started

### Prerequisites

- Java 23+
- Maven 3.9+
- Apache Tomcat 11+

---

### Clone Repository

```bash
git clone https://github.com/yourusername/VehicleRentalWebApp.git
cd VehicleRentalWebApp
```

---

### Build Project

Using Maven Wrapper

```bash
./mvnw clean package
```

or

```bash
mvn clean package
```

---

### Deploy

Deploy the generated WAR file

```text
target/VehicleRentalWebApp.war
```

into your Tomcat server.

---

### Initial Administrator Setup

Create the first administrator inside

```text
WEB-INF/admin.txt
```

Example

```text
admin:admin@example.com:Administrator:admin123
```

---

## 📸 User Workflow

1. Register a new account
2. Login
3. Browse vehicles
4. Select rental dates
5. Upload payment slip
6. Submit booking
7. Wait for admin approval
8. View notifications
9. Leave a review

---

## 🔒 Validation & Security

- Session-based authentication
- Role separation (User/Admin)
- File upload validation
- JPEG-only payment slips
- Maximum upload size (5MB)
- Rental date validation
- Servlet request validation

> **Note:** Passwords are currently stored as plain text because this project demonstrates file-based persistence. A production-ready implementation should use BCrypt hashing and database storage.

---

## 💡 Technical Highlights

- Java Jakarta EE MVC Architecture
- Servlet Annotation-Based Routing
- JSP Dynamic Pages
- Tailwind CSS Responsive UI
- File-Based Persistence
- Multipart File Upload
- Session Management
- Modular Project Structure
- Maven Build System

---

## 🔮 Future Improvements

- Migrate to MySQL or PostgreSQL
- BCrypt Password Encryption
- Spring Boot Migration
- REST API Implementation
- JWT Authentication
- Email Notifications
- Payment Gateway Integration
- Vehicle Availability Calendar
- Admin Analytics Dashboard
- Docker Deployment

---

## 👨‍💻 Developer

**F R M Fasri**  
**IT24102049**

BSc (Hons) Information Technology  
Specialization in Cyber Security

Sri Lanka Institute of Information Technology (SLIIT)

---

## 📫 Connect with Me

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/faz04)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/m-fasri/)

---

⭐ If you found this project helpful, consider giving it a star on GitHub!
