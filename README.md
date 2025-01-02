## Setup n8n and postgreSQL
Note: n8n is not support for mysql, so we need to use postgreSQL

1. Build postgreSQL at first
```
cd postgres
docker compose up -d
```

2. Setup user and database for n8n

- exec into postgreSQL container
```
docker exec -it postgres psql -U postgres
```

- create user and database for n8n
```
CREATE USER n8n_user WITH PASSWORD 'password';
CREATE DATABASE n8n_db;
GRANT ALL PRIVILEGES ON DATABASE n8n_db TO n8n_user;
```

3. Build n8n container
```
cd cluster
docker compose up -d
```

4. Access to n8n through browser: http://localhost:5678
5. Enjoy it!

## NOTE
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

3. Drop postgres user
```
DROP USER 'n8n_user_demo'@'n8n_db_demo'
```

