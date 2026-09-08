EO4WQ-NL responsive GitHub Pages build

This build has been optimized separately for desktop and mobile without changing
the public URL.

Desktop:
- full water-segment polygon geometry;
- existing desktop map behaviour retained.

Mobile/touch:
- lightweight point representation of all 7,820 segments;
- no thousands of Path2D polygons;
- no heavy country-outline Path2D;
- precomputed layer colours for fast layer switching;
- lower-resolution canvas;
- search, filters, zoom buttons and details remain available.

Timeline and lab observations are still loaded on demand.

To publish:
1. Replace the current repository contents with the contents of this folder.
2. GitHub Desktop: Commit to main.
3. Push origin.
