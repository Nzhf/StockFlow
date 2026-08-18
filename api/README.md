# StockFlow API (Laravel 12)

RESTful API backend for StockFlow inventory & order management system.

## Stack
- **Framework:** Laravel 12 (PHP 8.2+)
- **Database:** MySQL 8.0 (via Docker Compose)
- **Authentication:** Laravel Sanctum (Token-based API authentication)

## Local Setup
1. Ensure MySQL container is running:
   ```bash
   docker-compose up -d mysql
   ```
2. Copy environment file and generate key:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
3. Run migrations:
   ```bash
   php artisan migrate
   ```
4. Run dev server:
   ```bash
   php artisan serve
   ```

## Endpoints (Placeholder - Detailed docs added in Phase 2+)
- `POST /api/register`
- `POST /api/login`
- `POST /api/logout`
- `GET /api/user`
