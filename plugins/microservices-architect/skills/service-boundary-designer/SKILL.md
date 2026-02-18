---
name: service-boundary-designer
description: Design and validate microservice boundaries using Domain-Driven Design principles. Identifies tight coupling and suggests decomposition strategies.
---

# Service Boundary Designer

## When to use

- Starting a new microservices project
- Evaluating if a monolith should be decomposed
- Reviewing existing service boundaries for coupling issues
- Planning new features that span multiple services

## Instructions

1. **Identify Bounded Contexts**
   - Map business domains and subdomains
   - Find natural seams in the data model
   - Identify teams that own each domain

2. **Evaluate Coupling**
   - Flag synchronous chains longer than 2 hops
   - Identify shared database tables between services
   - Detect circular dependencies between services
   - Check for chatty interfaces (too many small calls)

3. **Suggest Decomposition**
   - Apply Single Responsibility Principle at service level
   - Recommend Strangler Fig pattern for monolith migration
   - Suggest CQRS where read/write patterns diverge significantly
   - Propose Saga pattern for distributed transactions

4. **Output**
   - Service boundary diagram (text-based)
   - Coupling score per service
   - Recommended refactoring steps
