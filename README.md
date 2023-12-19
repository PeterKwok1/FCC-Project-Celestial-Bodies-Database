# To do
Test unique and non null constraints
Join finished data
  Join and order?

# Dataset
https://en.wikipedia.org/wiki/List_of_galaxies
https://en.wikipedia.org/wiki/Lists_of_stars
https://en.wikipedia.org/wiki/Lists_of_planets
https://en.wikipedia.org/wiki/List_of_natural_satellites

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
