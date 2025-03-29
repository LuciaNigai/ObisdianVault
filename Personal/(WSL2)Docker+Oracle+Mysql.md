
## Oracle container
```
docker run -d \
  --name oracle-xe \
  -p 1521:1521 \
  -p 5500:5500 \
  -e ORACLE_PASSWORD=1122 \
  gvenzl/oracle-xe

```

## MySQL container
```
docker run -d \
  --name mysql-container \
  -p 3306:3306 \
  -e MYSQL_ROOT_PASSWORD=1122 \
  mysql:latest

```

### Oracle pdb and user
```
CREATE PLUGGABLE DATABASE my_pdb  
    ADMIN USER pdb_admin IDENTIFIED BY my_password  
    FILE_NAME_CONVERT = ('/opt/oracle/oradata/XE/pdbseed/',  
        '/opt/oracle/oradata/my_pdb/');  
  
  
ALTER PLUGGABLE DATABASE my_pdb OPEN;  
ALTER SESSION SET CONTAINER = my_pdb;  
  
CREATE USER my_user IDENTIFIED BY user_password;  
GRANT ALL PRIVILEGES TO my_user;  
  
ALTER SESSION SET CONTAINER = CDB$ROOT;
```

