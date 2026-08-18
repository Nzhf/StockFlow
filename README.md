# StockFlow

> **Inventory & Order Management System for Small Retail & F&B Businesses**

StockFlow is a full-stack inventory and order management system built with a decoupled Laravel 12 API backend and React (Vite) Single Page Application (SPA) frontend.

---

## 🏗 Architecture Overview

The system is structured as a single monorepo with independent backend and frontend directories:

```text
stockflow/
├── api/             # Laravel 12 REST API Backend (Sanctum Auth, MySQL, Eloquent)
├── web/             # React (Vite) SPA Frontend
├── .github/         # GitHub Actions CI Workflow
└── docker-compose.yml # Local MySQL 8.0 & phpMyAdmin services
```

- **Backend:** Laravel 12, MySQL 8.0, Laravel Sanctum for API token authentication.
- **Frontend:** React (Vite) SPA consuming Laravel REST API.
- **Data Integrity:** Database transactions for order placement with stock deduction rollbacks.
- **Code Quality:** Laravel Pint (PHP formatting), Prettier & Oxlint (React linting/formatting).

---

## 🚀 Quick Start (Local Development)

### Prerequisites
- PHP 8.2+ & Composer
- Node.js 20+ & npm
- Docker Desktop (for local MySQL database)

### 1. Database Setup
Start the local MySQL server and phpMyAdmin container:
```bash
docker-compose up -d
```
- MySQL running on `localhost:3306` (Database: `stockflow`, User: `stockflow`, Password: `stockflow_pass`)
- phpMyAdmin available at `http://localhost:8888`

### 2. Backend Setup (`/api`)
```bash
cd api
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
```
API server running at `http://localhost:8000`.

### 3. Frontend Setup (`/web`)
```bash
cd web
cp .env.example .env
npm install
npm run dev
```
Web app running at `http://localhost:5173`.

---

## 🧪 Testing & Formatting

### Backend
```bash
cd api
php artisan test
./vendor/bin/pint --test
```

### Frontend
```bash
cd web
npm run lint
npm run format:check
npm run build
```

---

## 📸 Screenshots
*(Screenshots will be added upon completing Phase 5 UI implementation)*

---

## 📜 License
MIT
