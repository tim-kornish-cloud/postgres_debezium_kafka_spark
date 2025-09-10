##Docker commands on command line

```code
~$ docker compose up -d
~$ docker exec -it postgres bash

root@postgres:/# psql -U postgres -d financial_db

financial_db=# select * from transactions;
```