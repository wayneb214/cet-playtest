# Assets and credits (v2, realistic)

Every texture and sky in this build is **CC0 (public domain)**, except the font (SIL OFL 1.1) and the water normal map (MIT). Nothing is paid, ripped or AI-generated. Buildings, terrain, trees, props and guests are built in code (`src/world/*`). The source files are downloaded by `assets-src/fetch.py` and converted by `assets-src/process.py`, `foliage.py` and `hdr.py`, which resize, colour-grade and pack them to KTX2 or JPG.

## Textures shipped in `public/tex/` (colour + normal map each)

| Shipped file | Source asset | Author / site | Licence |
|---|---|---|---|
| sand | `sand_03` | Poly Haven, polyhaven.com/a/sand_03 | CC0 |
| travertine (pool deck) | `floor_tiles_04` | Poly Haven | CC0 |
| terracotta (terraces, promenade) | `patio_tiles` | Poly Haven | CC0 |
| sandstone (sea wall, plinths) | `large_sandstone_blocks_01` | Poly Haven | CC0 |
| wood (jetty, loungers) | `wooden_planks` | Poly Haven | CC0 |
| stucco (walls) | `white_stucco_02` | Poly Haven | CC0 |
| roof | `clay_roof_tiles_02` | Poly Haven | CC0 |
| rock (cliffs, slopes) | `marble_cliff_02` | Poly Haven | CC0 |
| pinesand (hillside ground) | `forrest_sand_01` | Poly Haven | CC0 |
| bark | `bark_brown_02` | Poly Haven | CC0 |
| grass | `Grass005` | ambientCG, ambientcg.com/view?id=Grass005 | CC0 |
| roof2 (villas) | `RoofingTiles012A` | ambientCG | CC0 |
| pooltile | `Tiles107` | ambientCG | CC0 |
| fabric (parasols, cushions) | `Fabric030` | ambientCG | CC0 |
| foliage_atlas (olive, cypress, pine, broadleaf, oleander and bougainvillea cards) | leaf scans `LeafSet022`, `LeafSet024`, `LeafSet019`, `Foliage001`, composed by `foliage.py` | ambientCG | CC0 |
| palm_frond | leaflets cut from `Foliage001`, laid out by `foliage.py` | ambientCG | CC0 |
| waternormals | `waternormals.jpg` from the three.js examples | three.js authors | MIT |

## Skies and lighting (`public/hdr/`)

| Mode | HDRI | Site | Licence |
|---|---|---|---|
| Day | `kloofendal_48d_partly_cloudy_puresky` (Greg Zaal, Jarod Guest) | Poly Haven | CC0 |
| Golden hour | `qwantani_sunset_puresky` (Greg Zaal, Jarod Guest) | Poly Haven | CC0 |
| Night | `kloppenheim_02_puresky` (Greg Zaal, Jarod Guest) | Poly Haven | CC0 |

`hdr.py` decodes each 2k HDR, finds the sun position (written to `sky.json`) and saves the upper half as the visible sky JPG. The 1k `.hdr` files are used for image-based lighting.

These were downloaded for testing but are **not shipped**: Poly Haven `white_stucco`, `painted_plaster_wall`, `aerial_beach_01`, `bark_willow_02`, `bark_platanus`, `gravelly_sand`, `aerial_rocks_02`, `coast_sand_rocks_02`, `syferfontein_1d_clear_puresky`, `qwantani_noon_puresky`; ambientCG `Grass006`, `Tiles069`. All are CC0.

## Other

| Item | Source | Licence |
|---|---|---|
| Font: Nunito | Google Fonts, bundled as `src/assets/Nunito.ttf` | SIL Open Font License 1.1 |
| HUD icons | Hand-written inline SVG in `src/main.ts` | Original |
| Basis/KTX2 transcoder (`public/basis/`) | three.js `examples/jsm/libs/basis` | Apache 2.0 |
| Three.js r187 | npm `three` | MIT |
