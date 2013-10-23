---
layout: api-command 
language: Python
permalink: api/python/db_create/
command: db_create 
github_doc: https://github.com/rethinkdb/docs/edit/master/2-query-language/api/python/manipulating-databases/db_create.md
related_commands:
    db_drop: db_drop/
    db_list: db_list/
    table_create: table_create/
---

{% apibody %}
r.db_create(db_name) → object
{% endapibody %}

Create a database. A RethinkDB database is a collection of tables, similar to
relational databases.

If successful, the operation returns an object: `{"created": 1}`. If a database with the
same name already exists the operation throws `RqlRuntimeError`.
Note: that you can only use alphanumeric characters and underscores for the database name.

__Example:__ Create a database named 'superheroes'.

```py
r.db_create('superheroes').run(conn)
```


