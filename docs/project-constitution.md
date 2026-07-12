# Project Constitution

Version: 1.0  
Status: Active

---

# Purpose

This document defines the engineering principles, architecture rules, development workflow, and coding standards for the Coffeehouse platform.

Every architectural and implementation decision must comply with this constitution.

---

# Vision

Coffeehouse is a Telegram-native digital services platform.

It is designed to evolve from a VPN service into a complete marketplace for digital products without requiring fundamental architectural changes.

---

# Engineering Principles

- Simplicity over complexity
- Readability over cleverness
- Scalability over shortcuts
- Security by default
- Performance by design
- Documentation before implementation

---

# Architecture Principles

The project follows:

- Clean Architecture
- SOLID Principles
- Feature-Based Architecture
- Event-Driven Communication
- Repository Pattern
- Dependency Injection

---

# Repository Structure

```
apps/
packages/
docs/
docker/
scripts/
```

Each application must have a single responsibility.

---

# Monorepo

Applications:

- api
- admin
- miniapp

Shared packages:

- ui
- shared
- database
- providers
- telegram
- config

---

# Development Workflow

Every task follows:

1. Documentation
2. Architecture
3. Implementation
4. Testing
5. Review
6. Commit
7. Push

No feature is implemented before its documentation exists.

---

# Git Workflow

Branches:

- main
- develop

Rules:

- Never develop on `main`
- Daily work happens on `develop`
- `main` contains stable milestones only

---

# Commit Convention

Examples:

```
docs: add product vision

feat: implement wallet

fix: correct payment validation

refactor: simplify provider service

test: add wallet tests

chore: configure docker
```

---

# Backend Rules

Every feature module contains:

- controller
- service
- repository
- dto
- validators
- events
- tests

Business logic must never exist inside controllers.

---

# Frontend Rules

Frontend must be:

- Mobile-first
- Telegram-native
- Strict TypeScript
- Component-based
- Reusable

---

# Database Rules

- PostgreSQL
- Prisma ORM
- UUID primary keys
- Soft delete where appropriate
- Indexed foreign keys
- Explicit relationships

---

# Security

Always implement:

- Input validation
- Authentication
- Authorization
- Audit logging
- Rate limiting
- Secure secret management

---

# Documentation

Every major feature requires documentation before implementation.

Documentation lives under the `docs/` directory.

---

# Quality Standards

Every implementation must be:

- Production-ready
- Type-safe
- Tested
- Documented
- Maintainable

Temporary solutions are not accepted into the main codebase.

---

# Decision Making

When multiple solutions exist, choose the one that:

1. Reduces technical debt
2. Improves maintainability
3. Scales for future phases
4. Keeps modules loosely coupled

---

# Amendments

This constitution may evolve as the platform grows.

Any change must improve the long-term quality of the project without violating its core principles.