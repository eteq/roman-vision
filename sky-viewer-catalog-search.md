# Sky Viewer Science Case: Do catalog searches in the platform, show them on the sky in Roman, do data-mining tasks"

This example is a catalog-focused use case, demonstrating how one might start with catalogs and later need to interact with the sky viewer (unlike the others in this section, which are the other way around).

The user, Gandalf, is a very experienced astronomer who is fluent in Python but has been around a while so tends to have his own preferred way of doing things.  He has been influenced by his students, though (who are all for some reason very short...), and they 
after all these years they still manage to surprise him, in this case with the utility of the Roman Science Platform. Gadalf decides to try using it to search for resolved-star dwarf galaxies in the nearby universe.  

To do this, Gandalf pulls up the platform and works out a query (see the database access science cases for more details on how he might have done that part) to search through Roman source catalogs for point-sources that are consistent with being within the RGB star box of a dwarf galaxy at a certain distance.  For any given distance bin this is a relatively small dataset that can be run in a single notebook and doesn't require batch processing.  So he runs this for a specific distance bin beyond what ground-based surveys can do, and finds about a few thousand candidates.  The problem is, many of them are likely to be interlopers - e.g. chance alignments of stars or background unresolved galaxies. Gandalf manages to magically conjure up a few data mining tricks that lets him filter out some of these interlopers - this is easy to do on the platform because at these data sizes he can just make matplotlib plots like he's used to.  But he is still left with a few hundred candidates that require visual inspection.

Moreover, for this kind of visual inspection, he knows well that it's important to have groups of people do the inspection, because a single person will often convine themselves a candidate is real where a group will be more skeptical. So he decides to get together a group of postdoctoral fellows he's collaborating with to analyze the candidates, all in circular regions (this group ends up being called the Fellowship of the Ring, of course).  

He has produced color-magnitude diagrams for all the candidates, but he needs to give them access to the notebooks containing them, as well as a way to quickly run through them on the sky viewer.  So he generates one notebook per candidate, and places that within a Roman "group" on the platform, and gives the Fellowship access.  These notebooks, when run, grab the data for the candidates, plot the CMDs in a notebook cell, and show the target location on a sky viewer window in the platform interface.  The Fellowship members each run the notebooks one at a time, and if need be they might add a bit of their own code at the bottom to do extra analysis tasks if needed for that candidate to mine the data for the candidates they all agree are the best.

In the end they come up with a smaller but significant list of candidates.  Gandalf worries, though, that they data mined too greedily and too deep, so he wants to run some of his own software that he developed several years back to check these candidates.  He outputs the candidate source lists to a hand-tailored data table format, uploads his source code directory from an old laptop (or, on a good day, pip installs it), and uses the notebook terminal to run these scripts, which each take several hours. In the end, most are real, and the Fellowship find the first of many new dwarf galaxies discovered by Roman.  


### Addendeum

One of the non-candidates, though, turns out to be a much more massive galaxy, which for some reason they name... the Balrog... of Morgoth.  Time will tell if this has any negative consequences on cosmology.


### Question

Would an example of the notebook for the platform-oriented case be helpful here?  If so, I (EJT) can make that.