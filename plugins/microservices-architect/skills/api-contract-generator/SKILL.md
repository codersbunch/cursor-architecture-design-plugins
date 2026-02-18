---
name: api-contract-generator
description: Generate OpenAPI 3.0 specs, gRPC Protobuf definitions, and AsyncAPI event schemas from code or descriptions.
---

# API Contract Generator

## When to use

- Before implementing a new service endpoint
- When documenting existing APIs
- During API-first design sessions
- When setting up contract testing

## Instructions

1. **Analyze existing code** for route handlers, DTOs, and response types
2. **Generate OpenAPI 3.0 spec** with:
   - All endpoints with HTTP methods
   - Request/response schemas with examples
   - Authentication requirements
   - Error response definitions
3. **Generate Protobuf** for gRPC services with proper message types
4. **Generate AsyncAPI** for event-driven interfaces
5. **Add contract tests** using Pact or similar tools

## Output format

```yaml
openapi: 3.0.0
info:
  title: Service Name API
  version: 1.0.0
paths:
  /resource:
    get:
      summary: List resources
      responses:
        '200':
          description: Success
```
