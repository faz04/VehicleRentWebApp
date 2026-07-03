# VehicleRentalWebApp

A Java Jakarta EE web application for vehicle rental operations, featuring user registration, vehicle browsing, booking with payment slip upload, admin management, and text-file-based persistence.

## Key Features

- User registration and login
- Browse available vehicles with sorting options
- Book rentals with date validation and payment slip upload (JPEG, max 5MB)
- User dashboard for viewing bookings and notifications
- Admin login with full management access
- Admin vehicle management (add, edit, delete)
- Booking approval and rejection workflow
- Notifications management visible to users and admins
- Review submission and display for authenticated users
- File-based persistence using `WEB-INF` text files

## Architecture

- Java 23
- Maven WAR project
- Jakarta Servlet API 6.1.0
- JSP views powered by Tailwind CSS via CDN
- Data stored in `src/main/webapp/WEB-INF/` as plain text files
- Servlet annotations are used for request mappings

## Project Structure

- `src/main/java/` — application servlets and model classes
- `src/main/webapp/` — JSP pages and static assets
- `src/main/webapp/WEB-INF/` — application data files and deployment descriptor
- `pom.xml` — Maven build configuration

## Data Files

The application uses simple text files under `src/main/webapp/WEB-INF/`:

- `users.txt` — registered user accounts
- `admin.txt` — admin credentials
- `vehicles.txt` — available vehicle inventory
- `bookings.txt` — booking records
- `reviews.txt` — user reviews
- `notifications.txt` — notifications for users and admins

> Note: These files are empty by default, so initial admin credentials must be seeded manually before admin login.

## Setup and Run

### Prerequisites

- Java 23 or later
- Maven (or use provided Maven wrapper)
- A Jakarta EE-compatible servlet container such as Apache Tomcat 11+

### Build

From the project root:

```powershell
.\
\mvnw clean package
```

Or using Maven installed locally:

```powershell
mvn clean package
```

### Deploy

Deploy the generated WAR file found at:

```text
target\VehicleRentalWebApp.war
```

to your servlet container.

### Initial Admin Setup

Because `WEB-INF/admin.txt` starts empty, add a manual admin entry before logging in as admin. Use this format:

```text
admin:admin@example.com:Admin Name:adminpassword
```

Place the line in `src/main/webapp/WEB-INF/admin.txt` or the deployed container’s `WEB-INF/admin.txt`.

### First-Time User Setup

Register a user through the app interface at `register.jsp`. User data is appended to `WEB-INF/users.txt`.

## Usage

### Public Access

- Home page: `index.jsp`
- Vehicle listing: `vehicles`
- Reviews: `reviews`

### User Actions

- Register with a new account
- Login at `login.jsp`
- Book vehicles with start/end dates and upload JPEG payment slips
- View bookings and notifications on `dashboard`
- Submit reviews after login

### Admin Actions

- Login at `admin-login.jsp`
- Manage vehicles at `vehicle-management`
- Approve or reject bookings at `booking-management`
- Manage users, admins, and notifications from the admin dashboard

## Notes

- Passwords are stored in plain text in `WEB-INF` files.
- This app is best suited for learning, demo, or prototype use cases.
- For production use, replace text-file persistence with a database and add secure password hashing.

## Recommended Enhancements

- Replace file-based storage with a relational database
- Add password hashing and stronger authentication
- Improve session management and authorization checks
- Add image previews for uploaded payment slips
- Add input validation on the client side

## Contact

For questions or updates, inspect the servlet classes under `src/main/java/com/vehicle/rental/vehiclerentalwebapp/`.
