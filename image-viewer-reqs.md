# Image Viewer Requirements

Note: while titled "requirements", these are intentionally *not* framed as iron-clad requirements to be written aginst.  Rather they are categories of development and key relevant features.  This is because waterfall-style requirements are not compatible with a desire to to be agile in this process and being willing to adjust specific details to the  realities of limited development time and user feedback.

* Evaluate whether there are any completely missing features from the use cases in Imviz itself and plan for developing those. (EJT does not see any obvious ones, but the team will know better.)
* Develop and implement methods for easily transitioning into imviz from the sky viewer UI (detailed further in [entry point 1 and 2 of the base science case](image-viewer-base.md)).
* (Optional/stretch Goal): Allow imviz to be launched directly from a mission MAST search for RSP.
* Develop the layer/Python package that allows both the sky viewer and the image viewer to have a shared API for common operations (also referenced in the [sky viewer requirements](sky-viewer-reqs.md) and the [STScI image viewers RFF](https://innerspace.stsci.edu/x/rM0dFQ)).
* Ensure the capability exists to use standard astroquery.mast calls to "download" data into the RSP without actually doing any downloads, and have this easily loadable in imviz.  Document/maintian this is the standard way to access data so that viz-oriented notebooks are portable to other settings than the RSP.
* Ensure imviz data can be easily extracted from imviz in the RSP so that standard Python data analysis operations can be run on it (e.g. `photutils` aperture or PSF photometry).
* Ensure it's relatively straightforward to quickly and efficiently load science-case specific modified images into Imviz (a la the [psf photometry use case](image-viewer-psf-photometry.md)).  This includes difference images for time series use cases.
* Develop/ensure that a ramp visualization tool exists for Roman that is usable from the RSP.
* Develop the capability in the RSP (stretch goal: also from a user's laptop) to intelligently recognize which lower-level Roman images are relevant for specific pixels in a high-level image, and be able to launch the ramp viewer based on that determination. (Does not have to be via UI, can be code-based.)
* Ensure there are sufficient example notebooks demonstrating Imviz use in the RSP to reflect all of the use cases listed here.
* (Stretch Goal) State persistence from imviz - i.e., the ability to recover configuration that has been done via GUI after returning to a session after some break long enough that the kernel has shut down.
* (Stretch Goal) Develop tools that function in the RSP allowing long-running jobs that evolve out of a short-running/in-the-notebook operation (detailed further in the [aperture photometry science case](image-viewer-aperture-photometry.md). Note this may collide with other batch processing desires, and is a stretch goal in part for this reason.



