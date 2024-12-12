# "Time series focused Roman queries"

Authors: Gisella de Rosa and Susan Mullally


## Catalog Focused Use Cases.

For background, understand that Roman will have a rich set of catalogs developed by the mission and contributed by external teams. Catalog examples:

* Source catalogs that describe the location of known sources in the Roman fields.
* Forced Photometry Catalogs of extracted photometry for different fields, filters and times. This is just one example of a level 4 catalog.
* Catalogs of data availability. This could be CAOM or Roman level catalogs of data products.
* Catalogs containing science specific information - e.g. weak-lensing catalog, micro-lensing catalog

### Use Case 1.

A user would like to do color cuts on a source catalog to identify interesting sources (e.g. select potential high redshift QSOs).  For the selected sample, they might want to check on variability. To do so, they will need to want to find those sources in a forced photometry (likely doing a cross match, though some will only require an id look-up).  The users then will want to retrieve forced photometry values for a particular filters and create a plot (probably in lcviz) of photometry vs time for each filter. Another way to state this is to retrieve a table of time, filter, photometry for each object of interest.  Users then will want to calculate various metrics to figure out which light curves are “interesting” and select those objects for visualization with tools like matplotlib or lcviz.  This use case should be possible from catalogs. MAST, from the Roman Science Platform, or from a user’s laptop.  Note this overlaps heavily with the use cases in the [basic](database-access-base.md) and [extended](database-access-base.md) cases but has the added expectation that the catalogs also allow time as a search query.

### Use Case 1 b.

When an interesting target is found the user will want to inspect some of the level-2 data used create that forced photometry.  The user will want to retrieve a Roman tile for a source catalog position of interest and load it into imviz. The user may want to select particular times or filters or may just be happy with any one at random.  This overlaps heavily with Entry Point 3 in the [imviz viewer use case](image-viewer-base.md).

### Use Case 1 c.

For interesting targets, the user might also want to retrieve postage stamps from the difference images  (L5 products created and provided by the RAPID PIT)  and inspect them using imviz.  The user may want to retrieve photometry information from the catalog created from the difference images and plot the lightcurve. If catalogs are not available, the user might want to perform forced photometry on the difference images and create the lightcurves.

### Use Case 1d.

When a list of interesting targets are found, the user will want to determine if there are spectra available for those sources.  The user will then want to use specviz to inpsect some of those sources. The user will want to cross-match these sources to Euclid and Rubin catalogs held in the cloud and retrieve any forced photometry catalog points available for those sources.
