# Meteora 0.3: data notices

Meteora's landscape (the "site pack" inside the plug-in, in `Contents/Resources/pack`) is computed from two open
datasets. No survey or recording of the real site was used.

## Copernicus DEM

The terrain heights are produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus Defence and Space
GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved.

Tile `Copernicus_DSM_COG_10_N39_00_E021_00_DEM` (GLO-30, public instance), cut to the Meteora area, resampled from
30 m to 5 m and modified: the rock pillars are sharpened using OpenStreetMap cliff lines and summit heights.
Licence and terms: <https://dataspace.copernicus.eu/explore-data/data-collections/copernicus-contributing-missions/collections-description/COP-DEM>.

## OpenStreetMap

Contains information from [OpenStreetMap](https://www.openstreetmap.org/copyright), which is made available under
the [Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/).
© OpenStreetMap contributors.

OpenStreetMap features used: cliff lines, rock areas, summits (names and heights), monasteries, villages and
viewpoints in the Meteora area, fetched once through the Overpass API. They shape the pillars of the terrain, name
the rock faces (for example "Holy Spirit · N face"), and place the named listening positions.

### The OpenStreetMap-derived data is open

The site pack combines OpenStreetMap data with the elevation data, so it is a derivative database under the ODbL.
**The site pack files are made available under the ODbL 1.0**, separately from the plug-in software, whose own
licence (LICENSE.txt) does not restrict your rights in this data. The files are the complete derivative database,
free of charge in every download, in open, unencrypted formats: in the plug-in bundle at
`Meteora 0.3.vst3/Contents/Resources/pack/` (and the same in the app), described by its manifest `site.json`:

| file | what |
|---|---|
| `height.f32` | the stylised terrain heights, 5 m grid (float32, layout in `site.json`) |
| `patches.bin` | the acoustic surface patches derived from the terrain |
| `screen.glb` | the 3D terrain mesh shown on the panel (glTF) |
| `faces.json` | the named rock and ground faces |
| `positions.json` | the named microphone and source positions |
| `site.json` | the manifest: grid, sources, licences, stylisation summary and every stylised choice |

## What is simulated

Every sound Meteora makes is tagged *simulated from open data · uncalibrated*. The site pack's manifest
(`site.json`, field `stylised_or_non_physical`) lists every place where the model leaves the measured data or the
physics: the sharpened pillars, the two rock and ground materials, the visibility model, the surface model (trees and
roofs are part of the "ground"), and the choices of the ALIVE guide.
