This style intends to emulate the look of NYC DOT bike map (https://www.nyc.gov/html/dot/html/bicyclists/bikemaps.shtml). I've found this map is one of the best for displaying bike routes in a dense urban area, with a focus on edge cases most cycling styles ignore, like two-way bike routes on one way streets.

This style is to be used in conjunction with my fork of openmaptiles that adds cycling information from the OSM data set: https://github.com/thomasboyt/openmaptiles

Style todos:

- [ ] Better display of street names - move off of lines
- [ ] Tweak spacing of one way arrows
  - [ ] Potentially hide one-way arrows for short segments?
- [ ] Tweak zoom levels
- [ ] Better handling of adjacent bike paths of different types, e.g. Brooklyn Navy Yard's on-road lane and off-road lane

Rebuild openmaptiles:

```sh
# sometimes you might need to drop the db if things get weird
make destroy-db && make start-db-preloaded

# if only sql (no yaml!) changed
make clean && make all && make import-sql && make test-perf-null

# if yaml changed or pbf changed
make destroy-db && make start-db-preloaded && make clean && make all && make import-osm && make import-sql && make test-perf-null
```

To self-host sprites:

```sh
cd sprites
python -m http.server 4000
```