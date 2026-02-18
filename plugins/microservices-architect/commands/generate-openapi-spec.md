---
name: generate-openapi-spec
description: Generate a complete OpenAPI 3.0 specification from existing route handlers and DTOs in the codebase.
---

# Generate OpenAPI Spec

Scan the codebase and produce a complete OpenAPI 3.0 specification.

## Steps

1. Discover all route definitions (Express, FastAPI, Spring, etc.)
2. Extract request parameters, body schemas, and response types
3. Infer authentication from middleware
4. Generate schema definitions from DTOs/models
5. Add example values for all fields
6. Write spec to `docs/openapi.yaml`
7. Validate spec with `swagger-cli validate docs/openapi.yaml`
