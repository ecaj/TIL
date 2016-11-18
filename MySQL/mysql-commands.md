# MySQL Commands
```shell
# login as root
mysql -u root -p

# backup
mysqldump --opt -u [username] -p[password] [dbname] > [backupfile.sql]

# restore
mysql -u [username] -p[password] [dbname] < [backupfile.sql]
```
Note that there is no space between `-p` and `[password]`.

## Troubleshooting
If the above restoring method fails with `ERROR 1049 (42000): Unknown database [dbname]`, edit `[backupfile.sql]` and try adding these lines to the top :
```sql
CREATE DATABASE [dbname];
USE [dbname];
```

## Reference
- [ERROR 1049 (42000): Unknown database 'mydatabasename'](http://stackoverflow.com/questions/19678769/error-1049-42000-unknown-database-mydatabasename)
