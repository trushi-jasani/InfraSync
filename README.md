# 🏢 InfraSync – Apartment Management System

[![React](https://img.shields.io/badge/Frontend-React.js-61DAFB?logo=react&logoColor=white)](https://react.dev/)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Framework-Express.js-000000?logo=express&logoColor=white)](https://expressjs.com/)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

InfraSync is a **full-stack Apartment Management System** developed to simplify residential society operations by providing a centralized platform for administrators, managers, and residents.

The application enables apartment management, resident management, maintenance tracking, visitor management, parking allocation, and amenity booking through a secure role-based web application.

Built using **React.js, Node.js, Express.js, PostgreSQL, and JWT Authentication**, InfraSync follows a scalable three-tier architecture with a normalized relational database and secure RESTful APIs.

---

# ✨ Features

## 🔐 Authentication & Authorization

- JWT Authentication
- Role-Based Access Control (Admin, Manager, Resident)
- Protected API Routes
- Password Encryption using bcrypt

---

## 👥 Resident Management

- Register Residents
- Manage Resident Profiles
- Apartment Allocation
- Occupancy Tracking

---

## 🏢 Apartment Management

- Add/Edit/Delete Apartments
- Building & Floor Management
- Flat Availability Status
- Apartment Information Dashboard

---

## 🛠 Maintenance Management

- Raise Maintenance Requests
- Assign Maintenance Staff
- Track Request Status
- Update Completed Requests

---

## 🚗 Visitor Management

- Visitor Registration
- Entry & Exit Logs
- Resident Approval
- Visitor History

---

## 🚘 Parking Management

- Allocate Parking Slots
- Vehicle Registration
- Parking Availability Tracking

---

## 📅 Amenity Booking

- Book Community Hall
- Book Gym
- Book Garden
- Prevent Double Bookings

---

## 📢 Notice Board

- Society Announcements
- Event Notifications
- Emergency Notices

---

## 📊 Admin Dashboard

- Total Apartments
- Total Residents
- Maintenance Statistics
- Visitor Analytics
- Occupancy Reports

---

# 🛠 Tech Stack

## Frontend

- React.js
- React Router
- Axios
- CSS / Tailwind CSS

## Backend

- Node.js
- Express.js

## Database

- PostgreSQL

## Authentication

- JSON Web Tokens (JWT)
- bcrypt

## Tools

- Git
- GitHub
- Postman
- pgAdmin

---

# 🏗 Project Architecture

```
                 React.js Frontend
                        │
                 Axios HTTP Requests
                        │
               Express.js REST APIs
                        │
        Authentication Middleware (JWT)
                        │
          Controllers → Services → Models
                        │
                  PostgreSQL Database
```

---

# 🗄 Database Architecture

```
Users
│
├── Roles
│
├── Apartments
│      │
│      ├── Buildings
│      ├── Floors
│      └── Residents
│
├── Maintenance Requests
│
├── Visitors
│
├── Parking
│
├── Amenity Bookings
│
└── Notices
```

### Database Highlights

- 15+ Normalized Tables
- Foreign Key Constraints
- ON DELETE CASCADE
- Transaction Support
- Indexed Frequently Queried Columns
- ACID Compliant Design

---

# 📂 Folder Structure

```
InfraSync
│
├── client
│   ├── src
│   ├── components
│   ├── pages
│   ├── services
│   └── assets
│
├── server
│   ├── controllers
│   ├── models
│   ├── routes
│   ├── middleware
│   ├── config
│   ├── database
│   └── utils
│
├── package.json
├── README.md
└── .env
```

---

# 🚀 Getting Started

## Prerequisites

- Node.js (v18+)
- PostgreSQL
- Git

---

## Clone Repository

```bash
git clone https://github.com/trushi-jasani/InfraSync.git

cd InfraSync
```

---

# Environment Variables

Create a `.env` file inside the **server** folder.

```env
PORT=5000

DATABASE_URL=postgres://username:password@localhost:5432/infrasync

JWT_SECRET=your_secret_key

JWT_EXPIRES_IN=24h

NODE_ENV=development
```

---

# Install Dependencies

## Backend

```bash
cd server

npm install
```

## Frontend

```bash
cd client

npm install
```

---

# Run the Application

## Backend

```bash
cd server

npm run dev
```

---

## Frontend

```bash
cd client

npm start
```

---

# Database Setup

Create Database

```sql
CREATE DATABASE infrasync;
```

Run migrations (if available)

```bash
npm run migrate
```

Run seed files (if available)

```bash
npm run seed
```

---

# API Endpoints

## Authentication

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /api/auth/register | Register User |
| POST | /api/auth/login | Login |

---

## Apartments

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /api/apartments | Get Apartments |
| POST | /api/apartments | Add Apartment |
| PUT | /api/apartments/:id | Update Apartment |
| DELETE | /api/apartments/:id | Delete Apartment |

---

## Residents

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /api/residents | Get Residents |
| POST | /api/residents | Add Resident |

---

## Maintenance

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /api/maintenance | Get Requests |
| POST | /api/maintenance | Create Request |
| PUT | /api/maintenance/:id | Update Status |

---

## Visitors

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /api/visitors | Visitor List |
| POST | /api/visitors | Register Visitor |

---

## Parking

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /api/parking | Parking List |
| POST | /api/parking | Allocate Parking |

---

## Bookings

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /api/bookings | Get Bookings |
| POST | /api/bookings | Book Amenity |

---

## Dashboard

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /api/admin/dashboard | Dashboard Statistics |

---

# 🔒 Security Features

- JWT Authentication
- Password Hashing using bcrypt
- Protected Routes
- Role-Based Authorization
- SQL Injection Prevention
- Environment Variables
- CORS Configuration
- Input Validation

---

# ⚡ Performance Optimizations

- PostgreSQL Indexing
- Optimized SQL Queries
- Connection Pooling
- Modular Express Architecture
- Efficient REST APIs
- Lazy Loaded React Components

---

# 🎯 Highlights

- Full-Stack MERN-style Architecture (React + Node + PostgreSQL)
- JWT Authentication & Authorization
- PostgreSQL Database with 15+ Tables
- Normalized Relational Schema
- RESTful API Design
- MVC Backend Architecture
- Responsive React Frontend
- Secure Authentication
- Scalable Project Structure

---

# 👨‍💻 My Role – Database Designer & Administrator

I was responsible for designing and managing the complete database layer of the project.

### My Contributions

- 🗄️ Designed and implemented a normalized PostgreSQL database schema with **15+ relational tables**.
- 🔗 Established foreign key relationships to maintain referential integrity across the database.
- 📋 Created primary keys, unique constraints, check constraints, and cascade rules to ensure data consistency.
- 📊 Designed an efficient relational model for apartments, residents, maintenance requests, visitors, parking, and amenity bookings.
- ⚡ Optimized database performance by creating indexes on frequently queried columns.
- 🔄 Managed database connections and configuration between the Node.js backend and PostgreSQL.
- 💾 Created and maintained SQL scripts for database creation, schema updates, and data management.
- 🛡️ Ensured ACID-compliant transactions and data integrity throughout the system.
- 📈 Structured the database to support scalable CRUD operations and future feature expansion.



# 🚀 Future Enhancements

- Online Maintenance Payments
- Email Notifications
- Push Notifications
- QR Code Visitor Passes
- Resident Mobile App
- Real-Time Chat
- Complaint Analytics
- AI-Based Maintenance Prediction

---

# 📸 Screenshots

> Add screenshots of your application here.

```
Home Page

Dashboard

Resident Management

Maintenance Requests

Visitor Management

Apartment List
```

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository

2. Create your feature branch

```bash
git checkout -b feature/NewFeature
```

3. Commit changes

```bash
git commit -m "Add new feature"
```

4. Push branch

```bash
git push origin feature/NewFeature
```

5. Open a Pull Request

---

# 📄 License

This project is licensed under the MIT License.

---

# 👤 Author

**Trushi Jasani**

- GitHub: https://github.com/trushi-jasani
- LinkedIn: https://www.linkedin.com/in/trushi-jasani
- Email: jasanitrushi@gmail.com

---
