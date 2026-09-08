# EO4WQ-NL geographic map build

This version replaces the earlier flattened 0–1000 canvas geometry with the
original 7,820 WFD polygon geometries.

Core map CRS
- EPSG:3857 (Web Mercator) in the browser.
- Source geometries were extracted from `krw.shp` using the website's stored
  `source_row_index` and reprojected from EPSG:32631.
- The polygons and external imagery therefore share the same geographic map
  coordinates.

Background
- Plain: no external imagery requests.
- Satellite:
  - EOX Sentinel-2 Cloudless WMS is the seamless base.
  - PDOK current 25 cm RGB aerial WMTS tiles provide local high-resolution detail.
  - PDOK tiles are blended over the satellite base.

Performance
- Metadata/points load first.
- Simplified true polygon geometry (~5 m simplification) is a separate file.
- Desktop loads polygon geometry immediately.
- Mobile starts with points and loads polygons at local zoom or after selection.
- Timeline/lab shards are loaded only after segment selection.

Publish
1. Replace the contents of the local `nl-iron-map` repository with this folder.
2. Commit to main.
3. Push origin.
4. GitHub Pages remains configured from `main` / root.
