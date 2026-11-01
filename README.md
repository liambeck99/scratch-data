# Scratch places data

Weekly snapshots of places for the Scratch app: every café, restaurant, pub, bar and bakery in and around London, together with the borough boundaries (OSM admin level 8) around them.

Each release (`places-YYYY-MM-DD`) contains:

- `places.json.gz`: the snapshot, gzipped JSON.
- `manifest.json`: its format version, build and data dates, size, SHA-256 checksum and counts.

The app reads `https://github.com/Liambeck99/scratch-data/releases/latest/download/manifest.json`.

## Coverage and source

The snapshot covers the roughly 1 km grid cells over the London postcode areas E, EC, N, NW, SE, SW, W, WC, BR, CR, DA, EN, HA, IG, KT, RM, SM, TW, UB and WD. It's built from [Geofabrik](https://download.geofabrik.de/)'s England extract of OpenStreetMap with [osmium-tool](https://osmcode.org/osmium-tool/), keeping only these tags: `amenity=cafe`, `amenity=restaurant`, `amenity=pub`, `amenity=bar`, `shop=bakery`, and `boundary=administrative` with `admin_level=8`.

## Licence

The data is © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors, and is available under the [Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/). You may copy, distribute and adapt it, provided you attribute OpenStreetMap and share any adapted database under the same licence. The same attribution and licence are also recorded inside every `places.json.gz` and `manifest.json`.

This repository isn't affiliated with or endorsed by the OpenStreetMap Foundation.
