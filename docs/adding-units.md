# Add a catalog unit

1. Prepare the PNG using the [artwork guide](artwork.md). Save it as `artwork/<era-id>/<Faction>/<file>.png`. Match directory capitalization exactly. Git LFS tracks the PNG.
2. In [src/catalog.js](../src/catalog.js), copy an entry for the same unit type. Give it a unique stable `id`, a display `name`, the matching `era` and `faction`, the PNG basename in `file`, and a short `note`. Default names allow 20 characters including spaces, or 14 for Heroes. Register a new era in `eras` and give new factions a distinct entry in `factionGroundColors`.
3. Choose the rendering fields below. A battle role sets the initial formation. Users can change it independently of the number of figures drawn in the image.

| Assembled unit | Catalog fields | Existing entry to copy |
|---|---|---|
| Foot | `kind: 'Infantry'`, typically `height: 13.5`, with Warriors or Skirmishers as `defaultUnitType` | `gondor-rangers` |
| Cavalry | `kind: 'Mounted'`, typically `height: 20`, with Heavy Riders or Light Riders as `defaultUnitType` | `gondor-horse` |
| Hero | Foot or mounted kind, `hero: true`, 20 mm width and depth. Foot Heroes use `preserveAspect: true`. | `gondor-foot-captain` or `gondor-captain` |
| Monstrosity | `kind: 'Monster'`, 40 × 20 mm default base, explicit `uprightCount` and `panelHeight`, `preserveAspect: true` | `orc-ogres` |

When replacing artwork or renaming a unit, keep its ID. Saved quantities, roles, labels and roster assignments depend on it. The Giant retains `orc-troll` and Trolls retains `orc-monstrosities` with [orc-trolls.png](../artwork/middle-earth-third-age/Orcs/orc-trolls.png).

## Verify the result

Start the [workshop](../README.md#run-locally). Select the era and faction in Manual standees, add the new unit and download the PDF. Inspect both faces, figure count and weapon clearance. Print at actual size and check the ruler. For Cavalry or Monstrosities, compare the default and deeper bases. For a replacement, open an existing setup and confirm the unit still resolves.

Run the browser and PDF checks from the repository root. The tests start their own local server.

```sh
python3 -m venv .venv
.venv/bin/pip install -r requirements-dev.txt
.venv/bin/playwright install chromium
.venv/bin/python -m unittest discover -s tests -v
```
