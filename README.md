# School Management System API: Technical Challenge

This documentation outlines the implementation of a robust **School Management System API** built upon the **Axion** architectural framework. This project serves as a technical demonstration of system design, role-based access control (RBAC), and scalable backend architecture using Node.js, MongoDB, and Redis.

---

## 🏛 System Architecture

The project adheres to the **Axion** boilerplate structure, emphasizing a clear separation of concerns through specialized layers:

* **Managers**: The brain of the application where business logic and entity orchestration reside.
* **Loaders**: Responsible for bootstrapping the system, including database connections and service initialization.
* **Cortex**: A Redis-powered communication layer for high-performance data handling.
* **Connect**: Dedicated logic for MongoDB persistence and schema management.

---

## 🚀 Getting Started

### Prerequisites

* **Node.js**: v14+ (v18+ recommended for stability).
* **Database**: A running MongoDB instance (Local or Docker).
* **Cache**: A standard TCP Redis connection (e.g., [Upstash](https://upstash.com)).

### 1. Initialization

Clone the repository and install the core dependencies:

```bash
git clone https://github.com/AhsanRiaz9/axion
cd axion
npm install

```

### 2. Environment Configuration

Create a `.env` file from the provided template:

```bash
cp .env.example .env

```
And change .env values according to your services.
---

## 🛠 Core Functionalities

### 1. School Management (Superadmin)

The system provides a dedicated administrative layer for high-level management:

* **Provisioning**: Create and initialize new school entries.
* **Profile Control**: Full CRUD operations for school metadata.
* **Isolation**: Ensure data integrity across different school entities.

### 2. Role-Based Access Control (RBAC)

Security is implemented through a granular permission system:

* **Superadmin**: Global system access and school management.
* **School Admin**: Management of teachers, students, and school-specific settings.
* **Teacher/Student**: Restricted access to relevant academic resources.

---

## 🖥 Execution Guide

### Development Environment

To run the server with hot-reloading (via `nodemon`):

```bash
npm run dev

```

### Production Environment

To build and execute for high-performance environments:

```bash
npm start

```

*The default service port is **5111**.*

## 🧪 Quality Assurance

Maintain system integrity by running the automated test suite:

```bash
npm test

```

## 📖 API Documentation

A comprehensive **Swagger** definition is available in the root directory (`swagger.yaml`). This file outlines all available endpoints, required headers for RBAC, and expected request/response schemas.


API Docs URL: http://localhost:5111/docs