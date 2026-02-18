---
name: scaffold-service
description: Scaffold a new microservice with standard structure, Dockerfile, health checks, and CI config.
---

# Scaffold Microservice

Generate a production-ready microservice scaffold.

## Steps

1. Create directory structure:
   - `src/` - Application code
   - `tests/` - Unit and integration tests
   - `docs/` - OpenAPI spec
   - `scripts/` - Build and deploy scripts

2. Generate boilerplate:
   - Health check endpoint (`/health`, `/ready`)
   - Structured logging setup
   - Environment config with validation
   - Graceful shutdown handler

3. Add infrastructure files:
   - `Dockerfile` with multi-stage build
   - `docker-compose.yml` for local dev
   - `.github/workflows/ci.yml`
   - `k8s/` deployment manifests

4. Initialize with chosen framework (Express/FastAPI/Spring Boot)
