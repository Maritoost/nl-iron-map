EO4WQ-NL hybrid mobile map — final tested build

Desktop
- Full polygon map, unchanged.

Mobile
- Starts with lightweight points.
- Points remain while viewing broad regional scales.
- At local zoom (map width about 200 units or less), true water-segment polygons appear.
- Full geometry is fetched once, just before that threshold.
- Only polygons intersecting the current visible viewport are converted to Path2D and drawn.
- Zooming back out switches automatically to points.

Publish the complete contents of this folder to the existing nl-iron-map repository.
