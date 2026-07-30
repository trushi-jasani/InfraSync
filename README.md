
# InfraSync – Facility Management System 🏢⚡

[![Node.js](https://img.shields.io/badge/Node.js-v18.x-green.svg)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-v4.x-black.svg)](https://expressjs.com/)
[![React](https://img.shields.io/badge/React-v18.x-blue.svg)](https://reactjs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-v15.x-blue.svg)](https://www.postgresql.org/)
[![JWT](https://img.shields.io/badge/JWT-Secure-orange.svg)](https://jwt.io/)

InfraSync is an enterprise-grade, full-stack facility management system built to streamline multi-tenant facility scheduling, resource allocation, asset tracking, and issue reporting. The platform is architected with a heavily normalized PostgreSQL database schema (15+ tables) and robust RESTful APIs delivering sub-100ms response latencies.

---

## 🌟 Key Features

- **🔐 Role-Based Access Control (RBAC):** Granular middleware authentication with JSON Web Tokens (JWT) distinguishing between Administrators, Managers, and Standard Users.
- **📊 Interactive Admin Dashboard:** Real-time metrics for asset performance, maintenance schedules, and resource usage tracking.
- **⚡ Sub-100ms RESTful Endpoints:** Optimized database queries, strategic indexing, and streamlined routing for minimal network latency.
- **🗄️ Enterprise-Grade Database Architecture:** Normalized PostgreSQL database with 15+ relational tables, complex constraints, and transactional safety guarantees.
- **🛠️ Automated Maintenance Ticketing:** Integrated workflow allowing users to raise, assign, track, and update facility maintenance tickets.

---

## 🛠️ Tech Stack

- **Frontend:** React.js, Tailwind CSS / Modern CSS, Axios, React Router
- **Backend:** Node.js, Express.js
- **Database & ORM:** PostgreSQL, SQL / Knex.js / Prisma
- **Authentication & Security:** JSON Web Tokens (JWT), bcrypt hashing, CORS configuration
- **API Testing & Tools:** Postman, MySQL Workbench / pgAdmin, Git

---

## 🏗️ Database Architecture

InfraSync's backend is powered by a normalized PostgreSQL schema designed to scale safely:


```

[Users] <---> [User_Roles]
|
+---> [Tickets] <---> [Asset_Inventory] <---> [Facility_Locations]
|
+---> [Bookings] <---> [Resource_Schedules]

```

### Database Highlights:
- **15+ Relational Tables** handling multi-tenant resource data.
- **Strict Foreign Key Constraints & Cascades** for data consistency.
- **Indexed Primary & Foreign Keys** to keep query execution times consistently low under high loads.

---

## 🚀 Getting Started

Follow these instructions to set up and run InfraSync on your local machine.

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher)
- [PostgreSQL](https://www.postgresql.org/) (v14 or higher)
- [Git](https://git-scm.com/)

---

### 1. Clone the Repository

```bash
git clone [https://github.com/trushi-jasani/InfraSync.git](https://github.com/trushi-jasani/InfraSync.git)
cd InfraSync

```

---

### 2. Environment Variables Configuration

Create a `.env` file in the root directory (or inside server directory) with the following key-value pairs:

```env
PORT=5000
DATABASE_URL=postgres://your_pg_user:your_pg_password@localhost:5432/infrasync_db
JWT_SECRET=your_super_secret_jwt_key
JWT_EXPIRES_IN=24h
NODE_ENV=development

```

---

### 3. Database Setup

1. Open your PostgreSQL terminal or pgAdmin tool and create the database:
```sql
CREATE DATABASE infrasync_db;

```


2. Run database migrations and seed scripts (if applicable):
```bash
npm run db:migrate

```



---

### 4. Installation & Execution

#### Backend Setup

```bash
# Navigate to backend directory (if separate)
cd server
npm install
npm run dev

```

#### Frontend Setup

```bash
# Open a new terminal window, navigate to frontend directory
cd client
npm install
npm start

```

---

## 📌 API Endpoints Overview

| Method | Endpoint | Description | Access Level |
| --- | --- | --- | --- |
| `POST` | `/api/auth/register` | Register a new user | Public |
| `POST` | `/api/auth/login` | Authenticate & retrieve JWT token | Public |
| `GET` | `/api/facilities` | Fetch all available facilities | Authenticated |
| `POST` | `/api/tickets` | Create a new maintenance ticket | User / Manager |
| `GET` | `/api/admin/metrics` | Retrieve system analytics & statistics | Admin |

---

## 🎯 Technical Highlights for Recruiters

* **Database Performance:** Scaled and normalized PostgreSQL schema avoiding redundancy and ensuring high transactional integrity.
* **Security Best Practices:** Password hashing via bcrypt, environment abstraction, dynamic middleware authorization, and sanitized queries against SQL injections.
* **Maintainable Architecture:** Clean separation of concerns (Controllers, Models, Routes, Middlewares).

---

## 🛠️ My Role & Contributions: Core Database Engineer

As the Database Architect for InfraSync, I designed and implemented the entire database layer from scratch:
- **Schema Architecture:** Designed a heavily normalized PostgreSQL database schema with 15+ tables.
- **Data Integrity:** Configured foreign key relationships, cascades, and check constraints to guarantee ACID compliance and zero data redundancy.
- **Performance:** Designed strategic indexing on frequently queried columns (User IDs, Ticket Status, Timestamps) to ensure sub-100ms query execution.
- **Security:** Built server-side validation and prepared statements to protect against SQL Injection attacks.
## 👩‍💻 Author

**Trushi Jasani**

* **GitHub:** [@trushi-jasani](https://github.com/trushi-jasani)
* **LinkedIn:** [Trushi Jasani](https://www.linkedin.com/in/trushi-jasani-672396360/)
* **Email:** jasanitrushi@gmail.com
