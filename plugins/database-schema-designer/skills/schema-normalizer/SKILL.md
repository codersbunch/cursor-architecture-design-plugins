---
name: schema-normalizer
description: Analyze database schemas for normalization violations, redundancy, and structural issues. Suggests fixes up to 3NF/BCNF.
---

# Schema Normalizer

## When to use

- Reviewing new schema designs
- Auditing legacy schemas before migration
- When queries are slow due to data duplication
- Before major refactoring

## Instructions

1. **Check 1NF** - No repeating groups, atomic values only
2. **Check 2NF** - No partial dependencies on composite keys
3. **Check 3NF** - No transitive dependencies
4. **Check BCNF** - Every determinant is a candidate key
5. **Identify redundancy** - Duplicated data across tables
6. **Check index coverage** - Missing indexes on FK and filter columns
7. **Review data types** - Oversized VARCHAR, wrong numeric types
8. **Flag anti-patterns** - EAV, polymorphic associations, storing JSON blobs for structured data

## Output

- Normalization violations with table/column references
- Suggested normalized schema
- Migration SQL to fix issues
- Index recommendations
