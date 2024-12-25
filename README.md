## Setup n8n and mysql

1. n8n admin account
```
username: hieu.n@glasshouseventure.studio
password: vQ6jJnFy3guO5S
```

2. Create user n8n for postgreSQL database
```
CREATE USER n8n_user WITH PASSWORD 'password';
CREATE DATABASE n8n_db;
GRANT ALL PRIVILEGES ON DATABASE n8n_db TO n8n_user;
```
Note: n8n is not support for mysql, so we need to use postgreSQL

3. Drop mysql user
```
DROP USER 'n8n_user'@'localhost';
```

