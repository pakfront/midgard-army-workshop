# Midgard Army Workshop

Build a Midgard army roster and print matching paper miniatures. You can also pick standees directly from the Middle-earth, American Civil War, Napoleonic Wars and Wars of the Roses catalogs. The workshop runs in your browser and generates PDFs locally.

## Run locally

Clone with Git LFS installed so the checkout contains the PNG artwork and sample PDF. From the repository directory, run:

```sh
git lfs pull
./serve.sh
```

Open <http://localhost:8000>. The server requires Python 3 and accepts `--port 8080` to choose another port. For static hosting, serve `index.html`, `src/`, `vendor/` and the downloaded `artwork/` files together.

## From roster to tabletop

1. In **Army & battle roster**, create contingents and unit types, then add units and heroes under **Force**. Print the battle sheet with its points, reputation and trackers. Open the [Osgiliath example project](src/roster/osgiliath.json) to try a completed force.
2. In **Army standees**, assign artwork to each type and hero. You can override artwork by contingent and match the roster with labels and badges. For paper miniatures alone, use **Manual standees** to select artwork and quantities.
3. Choose paper size, base depth, ranks or riders, and label placement in **Print options**. Use **Save project** to keep a portable copy of the roster, artwork assignments and print settings.
4. Download the print PDF. Print single-sided at **100% / actual size** and measure the 40 mm ruler before cutting. To try assembly first, use the [starter PDF](examples/starter-print.pdf) and its [saved setup](examples/starter-setup.json).
5. Score the brown mountain folds and blue valley folds, then cut the solid outline. Glue each upright back-to-back with the printed faces outward. Valley-fold at the feet and glue the ground sections to the base. The workshop includes illustrated fold guidance.

## Contribute

Start with [making standee artwork](docs/artwork.md), then [add the unit to the catalog and check its print sheet](docs/adding-units.md). [Project instructions](AGENTS.md) cover saved-setup compatibility and contributor checks.

The roster editor was adapted from midgard-roster-maker revision `f2912cc`. See [profile data sources](docs/profile-sources.md). PDF export uses a bundled copy of pdf-lib 1.17.1 under its [MIT license](vendor/pdf-lib.LICENSE).

## AI generation and reuse

I used generative AI to create the workshop’s original code, documentation, and standee artwork. To the extent I hold copyright or related rights in my contributions, I dedicate those contributions to the public domain under [CC0 1.0 Universal](LICENSE). You’re welcome to use, modify, and share them without crediting me.

This dedication covers only rights I hold. The bundled pdf-lib library carries its own MIT license. Third-party rights in the Midgard material and the Middle-earth characters and setting remain with their respective owners.
