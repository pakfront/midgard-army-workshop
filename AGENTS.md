# Project instructions

Use the [artwork guide](docs/artwork.md) for unit types, base dimensions, figure density, style and panel composition. Follow [Add a catalog unit](docs/adding-units.md) for filenames, stable IDs, rendering fields and browser/PDF validation. Keep artwork paths and instructions current when changing the catalog.

## Preserve saved formations

All copies of a manually selected catalog unit share the battle role stored in `unitTypes` under its stable ID. Warriors use `ranks` (default 2), Skirmishers use `skirmisherRanks` (1), Heavy Riders use `riders` (4), and Light Riders use `lightRiders` (3). Preserve saved `ranks` and `riders` as Warriors and Heavy Riders in legacy setups and default missing settings. Heroes and Monstrosities keep their fixed upright counts.

For fold geometry or rendering changes, run the relevant browser/PDF tests in [tests/test_workshop.py](tests/test_workshop.py).
