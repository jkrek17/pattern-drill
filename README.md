# Pattern drill

A training game for marine forecasters: read GFS analysis maps around a low and call the wind ASCAT saw, now or 24 hours later.

- **Right now**: call the peak wind category (none, gale 34-47 kt, storm 48-63 kt, hurricane force 64+ kt): the strongest wind ASCAT saw anywhere on the map (the circled low is the deepest one), and tap where it is.
- **Forecast +24 h**: call grow, hold or decay, then the category.
- **Pairs**: two lows that looked alike but went opposite ways.
- **Benchmark**: a fixed 20-case check to take before and after practice.

174 cases from winters 2024-25 and 2025-26, North Atlantic and North Pacific. Stats stay in your browser.

This repository holds the built site only. The code that picks the cases and builds the deck is in `jkrek17/marine-research` (`studies/2026-11-05-pattern-drill/`); update this site with `page/export_site.py`.

Data: NOAA GFS analyses; NOAA GOES air-mass bands and GridSat-B1 infrared; ASCAT winds from Remote Sensing Systems. Training use only; not an official forecast product.

## Updating the site

From a clone of `jkrek17/marine-research`, after rebuilding the deck:

    python3 studies/2026-11-05-pattern-drill/page/export_site.py <path to this clone>

then commit and push here. GitHub Pages serves `main` from the root.
