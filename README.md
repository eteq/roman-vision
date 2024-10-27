# Roman Upscope Visioning Science Cases

## Sky Viewer

* [“Look for my favorite object and inspect it (all in MAST)”](sky-viewer-base.md)
* [“Find an object observed by Roman and identify other MAST data overlapping with it (+accessing catalogs via astroquery in platform)”](sky-viewer-catalog-search)
* [“Do catalog searches in the platform, show them on the sky in Roman, do various data-mining tasks”](sky-viewer-catalog-search)

## Image Viewer

* “Look at some faint objects near resolution limits and identify features only visible with careful stretching“ (low SB galaxies/UDGs) (also about transitioning from sky viewer to image viewer)
* “Go from sky-viewer to single-exposures to determine if a specific object is an artifact or not, including ramp view”
* "Do aperture photometry from the platform on a specific Roman image subset” (option on: large-scale processing)
* “Do PSF photometry from the platform on a specific Roman image subset“

MISSING?: Time-viz
MISSING?: cutouts

## Platform Database Access

* ["Starting from zero, gain some basic knowledge of what’s in a Roman source catalog, for someone who doesn’t know much about the mission."](database-access-base.md)
* “Start with some reasonable/common queries in the platform, then realize you need something esoteric, and ...
* “Cross-match a subset of a Roman catalog with a catalog that is also in some random part of AWS that is sizable but not enormous/batch-processing-needed.“
* “Write a dynamic query that the user specifies in galactic coordinates that then auto-translates to what the catalog sees“ (stretch goal: some wild and crazy helioprojective coordinate system)

MISSING?: Time-series analysis