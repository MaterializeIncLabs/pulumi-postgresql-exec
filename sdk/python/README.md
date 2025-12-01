# PostgreSQL Exec Pulumi Provider

> **Note:** This is a [Materialize](https://materialize.com) fork of [benesch/pulumi-postgresql-exec](https://github.com/benesch/pulumi-postgresql-exec), updated to use modern Pulumi SDK and fix the `pkg_resources` deprecation warning.

A [Pulumi](https://pulumi.com) provider that allows running arbitrary SQL
queries against a PostgreSQL database.

**Warning:** It is your responsibility to ensure that you supply both the
forward and reverse SQL statements.

## Usage example

To provision a PostgreSQL table:

```python
import pulumi_postgresql_exec as postgresql_exec

postgresql_exec.Exec(
    "create-table",
    create_sql="CREATE TABLE t (a int)",
    destroy_sql="DROP TABLE t",
)
```
