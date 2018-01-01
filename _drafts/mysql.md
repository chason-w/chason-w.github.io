## mysql





#### 1. about privileges

**查看授权**

```mysql
SHOW GRANTS;
```

> GRANT SELECT, INSERT, UPDATE, DELETE, CREATE, DROP, RELOAD, PROCESS, REFERENCES, INDEX, ALTER, SHOW DATABASES, CREATE TEMPORARY TABLES, LOCK TABLES, EXECUTE, REPLICATION SLAVE, REPLICATION CLIENT, CREATE VIEW, SHOW VIEW, CREATE ROUTINE, ALTER ROUTINE, CREATE USER, EVENT, TRIGGER, CREATE TABLESPACE ON *.* TO 'root'@'%' IDENTIFIED BY PASSWORD <secret> WITH GRANT OPTION

SHOW GRANTS 默认显示root/admin账号的授权，如果想要指定某个具体账号的授权，可以用

```mysql
SHOW GRANTS FOR user@host;
```

**授权**

```mysql
GRANT privileges ON db.table TO user@host [IDENTIFIED BY 'password'];
```
