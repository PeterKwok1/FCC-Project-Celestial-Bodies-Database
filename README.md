# To do
Plan 5 columns for each table
Test unique and non null constraints
Join finished data
  Join and order?

# Dataset
https://en.wikipedia.org/wiki/List_of_galaxies
https://en.wikipedia.org/wiki/Lists_of_stars
https://en.wikipedia.org/wiki/Lists_of_planets
https://en.wikipedia.org/wiki/List_of_natural_satellites

# Data planning
galaxy
  id - SERIAL
  name - VARCHAR
  origin - TEXT
star
  id - SERIAL
  name - VARCHAR
  mass - INT
planet
  id - SERIAL
  name - VARCHAR
  distance from sun - NUMERIC
  orbital_speed - INT
  has_life - BOOLEAN
moon
  id - SERIAL
  name - VARCHAR
  is_spherical - BOOLEAN
discovered_by
  id - SERIAL
  name - VARCHAR

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
