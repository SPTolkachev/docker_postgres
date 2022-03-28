# docker_postgres
Docker composition for Postgres and PgAdmin


## Install and run
1. Git clone.
```shell
git clone git@github.com:SPTolkachev/docker_postgres.git
```

2. Create `docker-compose.yml` from `docker-compose.yml.example`.
```shell
cp docker-compose.yml.example docker-compose.yml
```

3. Create `.env` from `.env.example` and change values.
```shell
~$ cp .env.example .env
~$ nano .env
```

4. Create dir data.
```shell
~$ mkdir data
~$ sudo chmod 777 data
```

5. Pull docker image.
```shell
~$ docker-compose pull
```

6. Run.
```
~$ docker-compose up -d
```

7. Open PgAdmin `http://localhost:5050` (if `PGADMIN_PORT=5050` in `.env`) in your browser. See email (`PGADMIN_EMAIL`) and password (`PGADMIN_PASSWORD`) in `.env`.


## Config .env
### Postgres
- `POSTGRES_VERSION` -- postgres' version
- `POSTGRES_PORT` -- postgres' port
- `POSTGRES_DB` -- postgres' datebase name
- `POSTGRES_USER` -- postgres' user login
- `POSTGRES_PASSWORD` -- postgres' user password

### PgAdmin
- `PGADMIN_PORT` -- PgAdmin's port
- `PGADMIN_EMAIL` -- PgAdmin's email (login)
- `PGADMIN_PASSWORD` -- PgAdmin's password
