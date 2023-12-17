# To do
Test unique and non null constraints

Restart
```
sudo service postgresql restart
```

Dump 
```
pg_dump -cC --inserts -U freecodecamp universe > universe.sql
```

Create
```
psql -U postgres < universe.sql
```
