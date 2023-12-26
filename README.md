# Dataset
- https://en.wikipedia.org/wiki/List_of_galaxies
- https://en.wikipedia.org/wiki/Lists_of_stars
- https://en.wikipedia.org/wiki/Lists_of_planets
- https://en.wikipedia.org/wiki/List_of_natural_satellites

# Data Structure 
galaxy
- id - SERIAL
- name - VARCHAR, NON NULL, UNIQUE
- origin - TEXT
- constellation - VARCHAR
- notes - TEXT

star
- id - SERIAL
- name - VARCHAR, NON NULL, UNIQUE
- mass_solar - INT
- distance_ly - INT
- galaxy_id - INT

planet
- id - SERIAL
- name - VARCHAR, NON NULL, UNIQUE
- distance_from_sun_km - NUMERIC
- has_life - BOOLEAN
- star_id - INT

moon
- id - SERIAL
- name - VARCHAR, NON NULL, UNIQUE
- radius_km - INT
- is_spherical - BOOLEAN
- planet_id - INT

discovery
- id - SERIAL
- name - VARCHAR, NON NULL, UNIQUE
- date - DATE
- galaxy_id - INT
- star_id - INT
- planet_id - INT
- moon_id - INT

# Commands
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
