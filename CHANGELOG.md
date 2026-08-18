# Changelog

All notable changes to the **StockFlow** project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added - Phase 0 (Setup)
- Scaffolding for decoupled architecture: `/api` (Laravel 12) and `/web` (React + Vite).
- Docker Compose configuration for local MySQL 8.0 database and phpMyAdmin.
- GitHub Actions CI pipeline running backend migrations/tests/Pint formatting and frontend linting/build checks.
- Foundational documentation: Root `README.md`, `api/README.md`, `CHANGELOG.md`.
