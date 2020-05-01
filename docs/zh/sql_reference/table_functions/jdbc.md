---
machine_translated: true
machine_translated_rev: b111334d6614a02564cf32f379679e9ff970d9b1
toc_priority: 43
toc_title: jdbc
---

# jdbc {#table-function-jdbc}

`jdbc(jdbc_connection_uri, schema, table)` -返回通过JDBC驱动程序连接的表。

此表函数需要单独的 `clickhouse-jdbc-bridge` 程序正在运行。
它支持可空类型（基于查询的远程表的DDL）。

**例**

``` sql
SELECT * FROM jdbc('jdbc:mysql://localhost:3306/?user=root&password=root', 'schema', 'table')
```

``` sql
SELECT * FROM jdbc('mysql://localhost:3306/?user=root&password=root', 'schema', 'table')
```

``` sql
SELECT * FROM jdbc('datasource://mysql-local', 'schema', 'table')
```

[原始文章](https://clickhouse.tech/docs/en/query_language/table_functions/jdbc/) <!--hide-->