# little-astro-scripts

Assorted scripts and notebooks for astronomy applications. All scripts use the CRAFT FRB20190608B (Macquart+20) as an example object. For any questions, comments, or concerns please open an issue send me an emailat alexagordon2026 [at] u.northwestern.edu.

## archival_imaging_query.ipynb

Notebook to query a coordinate's coverage in archival imaging and return available photometry and redshift estimates. Most importantly will calculate the happiness/sadness percentage based on how many surveys have field coverage.

## legacy_cutout.ipynb

Notebook to download a DESI Legacy Survey image cutout, make a smaller cutout, plot both, and optionally save as FITS files.

Available filters include g-, r-, and z-bands. Requires legacystamps package which can be downloaded via pip here: https://github.com/tikk3r/legacystamps.

## object_finder.ipynb

Notebook to generate a catalog and ds9 region file for sources within a box about a given position and radius from a Source Extractor catalog. Contains instructions on how to generate a Source Extractor catalog and load region file into ds9. Also includes code to calculate the positional uncertainty of a queried object.

# weighted_offsets.ipynb

Notebook to calculate weighted angular, physical (given redshift), and host-normalized (given host effective radius) offsets assuming the FRB (or other transient) localization is described by a 2D Gaussian. The code generates an oversampled grid of coordinates from the wcs of a field image (use legacy_cutout.ipynb or provide your own) and creates a distribution of angular offsets weighted by the localization probability map within 5sigma about the FRB localization, returning the median and 68% confidence intervals. If the redshift and host effective radius (aka half-light radius) are known, will also return physical (in kpc) and host-normalized (in r_e) offsets. Methodology first dveloped and presented in Gordon+25 (https://ui.adsabs.harvard.edu/abs/2025ApJ...993..119G/abstract). 