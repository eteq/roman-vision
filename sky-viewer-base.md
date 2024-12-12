# Sky Viewer Science Case: “Look for my favorite object and inspect it (all in MAST)”

This is essentially the base science case for the sky viewer - the simplest interactions astronomers expect.  Note that, unlike the other sky viewer cases, this one is intended to be implemented entirely via the MAST web site, not the science platform.
 
## Case 1: Starting form the Sky Viewer

The user follows a link directly to the sky viewer (akin to how a user right now will go straight to the MAST portal).  In this scenario, the user is an astronomer who knows the coordinates of some object they are interested in.  They enter the coordinates in a search box in the sky viewer *or* they provide it as part of the URL query string (e.g. something like http://mast.stsci.edu/romansky.html?ra=1.2&dec=3.4 ). This takes them immediately to a view centered on those coordinates with a base image that is optionally either 1) a full-sky ground-based image like DSS or perhaps a future LSST product, or 2) a tiled version of the Roman observations.  If possible, this should be 2 where present and 1 where not present.  They can pan and zoom as they wish once they've found their target and search for specific objects in the image that way.  The other workflows follow from this point.

For an existing example of this science case, go to https://www.legacysurvey.org/viewer?ra=39.9685&dec=-34.4705&layer=ls-dr9&zoom=12 - while this is a ground-based data set, the sky viewer idiom is perfect (and well-liked in the astronomy community).

## Case 2: Starting from a Search Interface

The user begins in a mission-mast interface akin to the existing HST/JWST interfaces (https://mast.stsci.edu/search/ui/#/hst and https://mast.stsci.edu/search/ui/#/jwst) or the search interface for the portal. The user searches for a specific target by name, and finds a long list of Roman exposures for this target.  They are immediately confused by the sheer number of observations and data products because the target is in one of the survery regions. But they see a sky-viewer button (either as a "show this search in the sky viewer" or a little icon next to the row of the search a la the current icons that open up jdaviz for jwst searches), and click on it.  The result is a view like case 1, but with the specific search's observations highlighted akin to the current portal searches - i.e. footprints that you can click on and see additional observation-specific information.  They can pan and zoom as they wish once they've found their target and search for specific exposures or objects in the image that way.  The other workflows follow from this point.

## Notes

* Case 1 is *not* the same as the current MAST portal, in that it should display some base image even when no search has yet been done.  What the "base image" is doesn't need to be determined at this time, and indeed should be flexible enough to change with time. I.e., it might start out as a DSS or Legacy Survey base image, but later get Rubin and Roman wide added as base map options as time passes and those surveys become complete enough to be useful.
* Note that all the other sky-viewer cases consider the perspective of starting from the science platform, so while that isn't highlighted here, that's intentional.