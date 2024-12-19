# Sky Viewer Requirements

Note: while titled "requirements", these are intentionally *not* framed as iron-clad requirements to be written aginst.  Rather they are categories of development and key relevant features.  This is because waterfall-style requirements are not compatible with a desire to to be agile in this process and being willing to adjust specific details to the  realities of limited development time and user feedback.

* Development of a sky viewer that supports "sky first" search - i.e., a sky viewer that has a visible basemap before any mission or CAOM search is done.
* Integration of a base map for the sky viewer that is relevant for Roman, and support for updating to include Roman imaging. (See [the base case](sky-viewer-base.md) for specific details.)
* Development of basic sky viewer functionality - pan, zoom, coordinates overlay, etc. (Note that this may simply be "adopt an existing viewer like Aladin Lite which already has these features".)
* Integration of linking to the sky viewer from a Roman mission mast search.
* Observation/footprint overlays in the sky viewer from MAST missions (esp Roman, JWST, HST).
* Integration of a sky viewer panel that works in Jupyterhub and the RSP that can be controlled via notebook.
* Ability to overplot catalogs via the RSP notebook API. Stretch goal: keyboard based automatic panning to elements of a catalog (see [other data use case](sky-viewer-other-data.md) for more details). (Note: this requirement intentionally does *not* include plotting from a GUI-based catalog querying. That could be added in the future, but is much lower priority than the reqs here.)
* Integration with Image Viewer (more details in (the image viewer requirements)[image-viewer-reqs.md]).
* RSP-oriented notebooks that demonstrate all of the above functionality.