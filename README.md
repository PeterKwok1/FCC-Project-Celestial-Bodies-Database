# To do
Test unique and non null constraints
Join finished data
  Join and order?

# Dataset
https://en.wikipedia.org/wiki/List_of_galaxies
https://en.wikipedia.org/wiki/Lists_of_stars
https://en.wikipedia.org/wiki/Lists_of_planets
https://en.wikipedia.org/wiki/List_of_natural_satellites

# Data Structure 
galaxy
  id - SERIAL
  name - VARCHAR, NON NULL, UNIQUE
  origin - TEXT, NON NULL
  constellation - VARCHAR
  notes - TEXT
star
  id - SERIAL
  name - VARCHAR, NON NULL, UNIQUE
  mass - INT, NON NULL
  distance_ly - NUMERIC
  notes - TEXT
planet
  id - SERIAL
  name - VARCHAR, NON NULL, UNIQUE
  distance from sun - NUMERIC, NON NULL
  orbital_speed - INT
  has_life - BOOLEAN
moon
  id - SERIAL
  name - VARCHAR, NON NULL, UNIQUE
  parent - VARCHAR, NON NULL
  is_spherical - BOOLEAN
  radius_km - INT
discovery
  id - SERIAL
  name - VARCHAR, NON NULL, UNIQUE
  date - DATE, NON NULL
  galaxy_id - INT
  star_id - INT
  planet_id - INT
  moon_id - INT

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
