############################################################################
#
#  velocity.zip
#
#  Data from:  Biotic and climatic velocity identify contrasting areas of vulnerability to climate change
#  Carroll, Carlos, Lawler, Joshua J., Roberts, David R., and Hamann, Andreas. 
#  Published in: PLOS One (2015)
#  
############################################################################

This zip file includes raster data representing biotic and climatic velocity for the Western Hemisphere for the period 1961 to 2100. We modeled velocity using climatic niche models originally published in:

Joshua J. Lawler, Sarah L. Shafer, Denis White, Peter Kareiva, Edwin P. Maurer, Andrew R. Blaustein, and Patrick J. Bartlein 2009. Projected climate-induced faunal change in the Western Hemisphere. Ecology 90:588-597. http://dx.doi.org/10.1890/08-0823.1.

We used the code in the included R script to model biotic velocity for each individual species in Lawler et al. (2009). We then summarized velocity across all species in the three taxa groups, and further summarized across 10 climate-change general circulation models. We also modeled climatic velocity for each of 10 climate-change general circulation models. Each data file is a 50-kilometer resolution ESRI ASCII grid.

All calculations were performed using R statistical software (http://www.r-project.org/). 

Please see http://adaptwest.databasin.org for additional spatial data and documents related to this study. 

############################################################################

File Naming convention:

[TYPE][GCM][DIRECTION].asc

[TYPE] - Type of data

climate		climatic velocity
amphibians	biotic velocity derived from SDMs for 413 amphibian species
birds		biotic velocity derived from SDMs for 1818 bird species
mammals		biotic velocity derived from SDMs for 723 mammal species

[GCM]

cccma_cgcm3.1_t47_run1
cnrm-cm3_run1
gfdl-cm2.0_run1
gfdl-cm2.1_run1
giss-er_run1
inm-cm3.0_run1
miroc3.2_medres_run1
mri_cgcm2.3.2a_run1
ncar_ccsm3.0_run1
ukmo-hadcm3_run1	

[DIRECTION] - Type of analysis
	
fwd		forward velocity (km/year)
bwd		backward velocity (km/year)
disp		proportion of species disappearing (biotic velocity) or proportion of runs with disappearing climates (climatic velocity)


*.asc		The file extension .asc denotes ESRI ASCII grid format.

############################################################################

Contents of *.asc files:

First six lines:
NCOLS = number of columns in grid
NROWS = number of rows in grid
XLLCORNER = x coordinate of lower left corner (corner, not center of cell)
YLLCORNER = y coordinate of lower left corner (corner, not center of cell)
CELLSIZE = length of a single side of each cell, in meters
NODATA_value = The value that denotes missing data.

Remaining lines:

Data separated by spaces. A carriage return (\n) denotes the next row of the
grid.

############################################################################

Coordinate system and projection parameters (also given in file cylindricalEqualAreaSphere.prj)

Projection    CYLINDRICAL                                                       
Zunits        NO                                                                
Units         METERS                                                            
Spheroid      SPHERE                                                            
Xshift        0.0000000000                                                      
Yshift        0.0000000000                                                      
Parameters                                                                      
            1 /* Projection type < 1 | 2 | 3 >                                 
 0  0  0.000 /* Longitude of central meridian                                   
 30  0  0.000 /* Latitude of standard parallel 

############################################################################

Additional enclosed files:

README.txt			This file
cylindricalEqualAreaSphere.prj	Coordinate system and projection parameters. File format compatible with ArcGIS Desktop <= 10.1
Carrolletal_S1_File.txt		R code to calculate climatic and biotic velocity

############################################################################









