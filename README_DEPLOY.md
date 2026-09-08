# EO4WQ-NL geographic FAST build

This is a performance-optimised version of the geographically correct map.

What changed
- Initial segment metadata reduced from ~6.2 MB to ~1.6 MB by compact encoding.
- The first screen does not block on detailed geometry.
- Desktop shows points immediately, then swaps to true 50 m-simplified polygons
  once a ~0.6 MB coarse geometry file has loaded.
- Mobile remains point-first and loads polygons only after local zoom/selection.
- Detailed 5 m true geometry is delta-encoded (~1.5 MB) and fetched only at close
  zoom or after selecting a segment.
- Canvas polygon paths are built once and cached as Path2D objects.
- Drawing uses a geographic world-to-screen canvas transform, instead of
  reconstructing every polygon in screen coordinates on every frame.
- Only visible segments are drawn.
- Satellite imagery still loads only when Satellite is selected.

Geographic alignment is unchanged
- True 7,820 WFD geometries.
- Browser map: EPSG:3857.
- No guessed canvas-to-map transform.

Publish
1. Replace the contents of your local `nl-iron-map` repository with this folder.
2. Commit to main.
3. Push origin.
