---
name: migration-generator
description: Generate safe, reversible database migrations from schema changes. Supports Postgres, MySQL, and common ORMs.
---

# Migration Generator

## When to use

- Adding new tables or columns
- Modifying existing schema
- Creating or dropping indexes
- Renaming tables or columns safely

## Instructions

1. **Analyze the schema diff** between current and desired state
2. **Generate up migration** with:
   - CREATE/ALTER TABLE statements
   - Index creation
   - Data backfill if needed
   - Constraint additions
3. **Generate down migration** (rollback) for every change
4. **Safety checks**:
   - Flag column drops (data loss risk)
   - Warn on NOT NULL additions without defaults
   - Suggest concurrent index creation for large tables
   - Check for lock-heavy operations on production tables
5. **ORM format** - Output for Knex, Prisma, Alembic, Flyway, or Liquibase

## Output

```sql
-- Up migration
ALTER TABLE users ADD COLUMN phone VARCHAR(20);
CREATE INDEX CONCURRENTLY idx_users_phone ON users(phone);

-- Down migration
DROP INDEX idx_users_phone;
ALTER TABLE users DROP COLUMN phone;
```
