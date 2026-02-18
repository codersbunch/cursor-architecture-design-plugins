---
name: generate-migration
description: Generate a safe, reversible database migration file from schema changes with up and down methods.
---

# Generate Migration

Create a complete migration file from the current schema changes.

## Steps

1. Detect schema changes from model/entity definitions
2. Generate timestamped migration file
3. Write `up()` with all forward changes
4. Write `down()` with complete rollback
5. Add safety warnings for destructive operations
6. Validate migration syntax
7. Run `dry-run` to preview SQL without executing
