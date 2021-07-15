# ahk-latlon-geohash
Implement latlon-geohash in autohotkey.

geohash
=======

Functions to convert a [geohash](http://en.wikipedia.org/wiki/Geohash) to/from a latitude/longitude
point, and to determine bounds of a geohash cell and find neighbours of a geohash.

It's conversion by [latlon-geohash](https://github.com/chrisveness/latlon-geohash).

API
---

- `Geohash.encode(lat, lon, [precision])`: encode latitude/longitude point to geohash of given precision
   (number of characters in resulting geohash); if precision is not specified, it is inferred from
   precision of latitude/longitude values.
- `Geohash.decode(geohash)`: return { lat, lon } of centre of given geohash, to appropriate precision.
- `Geohash.bounds(geohash)`: return { sw, ne } bounds of given geohash.
- `Geohash.adjacent(geohash, direction)`: return adjacent cell to given geohash in specified direction (N/S/E/W).
- `Geohash.neighbours(geohash)`: return all 8 adjacent cells (n/ne/e/se/s/sw/w/nw) to given geohash.