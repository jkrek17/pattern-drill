# Training

Training drills for marine forecasters, on real past storms and judged against what was observed. Stats stay in your browser.

- **Wind drill** (`wind/`): read model maps around a storm and call the strongest wind ASCAT saw or will see (none, gale 34-47 kt, storm 48-63 kt, hurricane force 64+ kt).
  - **Right now**: maps at the time of an ASCAT pass.
  - **Beat the model**: GFS and ECMWF +24 h forecast maps; your score is set against the models' own and against 925 mb wind × stability.
  - **Storm or HF?**: storm force or more on every map; is it 48-63 kt or 64+?
  - **Benchmark**: 20 fixed Beat the model cases to take before and after practice.
  - 334 cases over the five winters 2021-26, North Atlantic and North Pacific.
- **Front drill** (`fronts/`): draw the fronts on real storms (North Atlantic and Northeast Pacific) and compare with the Unified Surface Analysis; 522 cases.

This repository holds the built site only. The code is in `jkrek17/marine-research`: the wind drill in `studies/2026-11-05-pattern-drill/` and the front drill in `studies/2026-11-06-front-drill/`.

Data: NOAA GFS analyses and forecasts; ECMWF open data; NOAA GOES air-mass bands and GridSat-B1 infrared; ASCAT winds from Remote Sensing Systems; WPC/OPC coded surface analyses. Training use only; not an official forecast product.

## Updating the site

From a clone of `jkrek17/marine-research`:

    python3 studies/2026-11-05-pattern-drill/page/export_site.py <path to this clone>   # landing page + wind/

then commit and push here. The front drill thread writes `fronts/` with its own export. GitHub Pages serves `main` from the root.
