## Docker commands on command line

set up containers
```code
~$ docker compose up -d
```
start up connection to postgres in console
```code
~$ docker exec -it postgres bash
```
connect to financial db in postgres
```code
root@postgres:/# psql -U postgres -d financial_db
```
select records from transaction table
```code
financial_db=# select * from transactions;
```

## create connection to debezium

### conneciton through UI
1) select db conneciton type
2) fill out properties of connection
3) change replication Plugin to pgoutput
4) review and connect

{
  "connector.class": "io.debezium.connector.postgresql.PostgresConnector",
  "topic.prefix": "cdc",
  "database.user": "postgres",
  "database.dbname": "financial_db",
  "database.hostname": "postgres",
  "database.password": "********",
  "name": "postgres_financial_connector",
  "plugin.name": "pgoutput"
}

### conneciton through Console