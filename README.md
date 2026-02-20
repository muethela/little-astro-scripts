# little-astro-scripts

Assorted scripts and notebooks for astronomy applications. All scripts use FRB20190608B as an example object.

## legacy_cutout.ipynb

Notebook to download a DESI Legacy Survey image cutout, make a smaller cutout, plot both, and optionally save as FITS files.

Available filters include g-, r-, and z-bands. Requires legacystamps package which can be downloaded via pip here: https://github.com/tikk3r/legacystamps.

## archival_imaging_query.ipynb

Notebook to query a coordinate's coverage in archival imaging and return available photometry and redshift estimates. Most importantly will calculate the happiness/sadness percentage based on how many surveys have field coverage.

## object_finder.ipynb

Notebook to generate a catalog and ds9 region file for sources within a box about a given position and radius from a Source Extractor catalog. Contains instructions on how to generate a Source Extractor catalog and load region file into ds9. Also includes code to calculate the positional uncertainty of a queried object.