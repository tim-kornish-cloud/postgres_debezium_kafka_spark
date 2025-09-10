##Docker commands on command line

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