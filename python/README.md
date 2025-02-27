## DEMReg python

This is a python version of the "mapping" DEMReg code which you can find in this repo in [../idl/](../idl/). 

This repo contains main python code needed and some nice jupyter notebook examples:
* [example_demregpy_aiasyn.ipynb](https://github.com/ianan/demreg/blob/master/python/example_demregpy_aiasyn.ipynb) Example notebook recovering the DEM from synthetic AIA data
* [example_demregpy_aiapxl.ipynb](https://github.com/ianan/demreg/blob/master/python/example_demregpy_aiapxl.ipynb) Example notebook recovering the DEM from real AIA data, including how to prep it via aiapy
* [ex_demregpy_regionerr.ipynb](https://github.com/ianan/demreg/blob/master/python/ex_demregpy_regionerr.ipynb) Example notebook using synthetic data and plotting final DEMs as error regions instead of errobars
* [dn2dem_pos.py](https://github.com/ianan/demreg/blob/master/python/dn2dem_pos.py) Wrapper to use data (single set or map) with demmap_pos.py
* [demmap_pos.py](https://github.com/ianan/demreg/blob/master/python/demmap_pos.py) Main DEMReg code (input is spatial 1D of data)

Main development was by Alasdair Wilson see [https://github.com/alasdairwilson/demreg-py](https://github.com/alasdairwilson/demreg-py), with examples there for working with AIA maps.

If you use this code please reference back to [Hannah & Kontar (2012)](https://doi.org/10.1051/0004-6361/201117576) and [Hannah & Kontar (2013)](https://doi.org/10.1051/0004-6361/201219727).

## Potted history

* The original SSWIDL code to obtain the Differential Emission Measure (DEM) from solar data using regularized inversion in sswidl, DEMReg, is the one featured in [Hannah & Kontar (2012)](https://doi.org/10.1051/0004-6361/201117576) and in the repo in [../idl_org/](../idl_org/)
* This was based on the regularization code of [Kontar et al (2004)](https://doi.org/10.1007/s11207-004-4140-x) which is for (RHESSI) X-ray spectrum inversion. It implements [Hansen (1992)](https://doi.org/10.1088/0266-5611/8/6/005) GSVD version of [Tikhonov (1963)](https://scholar.google.com/scholar_lookup?author=Tikhonov%2C+A.+N.&journal=Soviet+Math.+Dokl.&volume=4&pages=1035&publication_year=1963) regularization.
* A faster/parallized version of [demreg](http://www.astro.gla.ac.uk/~iain/demreg/map/) was developed for working with SDO/AIA maps. This "mapping" version of the code was featured in [Hannah & Kontar (2013)](https://doi.org/10.1051/0004-6361/201219727). An updated version of this code, with bug fixes, and to work with a variety of data (not just SDO/AIA) is the version now available in this repo in [../idl/](../idl/) (it, howvere, is not currently parallized - no IDL Bridges) The python version here is based on this idl version.
* A previous non-public python version of the original DEMReg was developed and used by Erwin Verwichte and Petra Kohutova in [Kohutova & Verwichte (2016)](https://doi.org/10.3847/0004-637X/827/1/39) and [Verwichte & Kohutova (2017)](https://doi.org/10.1051/0004-6361/201730675).
* There might be other versions out there .....

