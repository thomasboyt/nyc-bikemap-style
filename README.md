This style intends to emulate the look of NYC DOT bike map (https://www.nyc.gov/html/dot/html/bicyclists/bikemaps.shtml). I've found this map is one of the best for displaying bike routes in a dense urban area, with a focus on edge cases most cycling styles ignore, like two-way bike routes on one way streets.

This style is to be used in conjunction with my fork of openmaptiles that adds cycling information from the OSM data set: https://github.com/thomasboyt/openmaptiles

Todos:

- [ ] Better display of street names - move off of lines
- [ ] One way arrows
- [ ] Tweak zoom levels
  - [ ] Display cycleways (e.g. bridge lanes) below 11 (requires openmaptiles change)
- [ ] Better handling of adjacent bike paths of different types, e.g. Brooklyn Navy Yard's on-road lane and off-road lane
