# EventConnect Ghana — Application Architecture

## 1. Architecture Style

The application will use a modular monolith architecture.

The frontend and backend will be logically separated.
The backend will contain independent feature modules within
a single Express application.

## 2. Frontend

Technologies:
- HTML
- CSS
- JavaScript

Responsibilities:
- Display service listings
- Search and filter providers
- Manage customer interactions
- Display customer dashboards
- Display provider dashboards
- Display administrator dashboards

## 3. Backend

Technologies:
- Node.js
- Express.js

Modules:
- Authentication
- Users
- Providers
- Categories
- Services
- Bookings
- Quotations
- Reviews
- Notifications
- Administration

## 4. Database

Technology: PostgreSQL

Responsibilities:
- Store user accounts
- Store provider profiles
- Store service categories
- Store service listings
- Store booking requests
- Store quotations
- Store reviews
- Store notifications
- Maintain booking history

## 5. File Storage

Provider images will be stored in object storage.

PostgreSQL will store image metadata and object references.

## 6. Infrastructure

Development:
- Docker
- Docker Compose
- PostgreSQL
- Node.js
- Nginx

Production:
- AWS
- HTTPS
- Nginx
- Dockerized application
- Managed PostgreSQL where appropriate
- Object storage
- Automated backups
- Application monitoring

## 7. Request Flow

1. A customer visits the website.
2. The frontend sends an HTTP request to the backend API.
3. The backend validates the request.
4. Authentication and authorization are checked where required.
5. The backend executes the necessary business logic.
6. PostgreSQL stores or retrieves the required data.
7. The backend returns a response.
8. The frontend displays the result.

## 8. API Versioning

API prefix:

/api/v1

## 9. Architectural Principles

- Keep business logic separate from HTTP routing.
- Validate incoming data.
- Enforce permissions in the backend.
- Use database transactions for related changes.
- Keep credentials outside source control.
- Write automated tests.
- Use database migrations.
- Avoid unnecessary microservices.

