Metadata
========

Title: Africa Rainfall Project Data
Summary: Data are high-resolution computer simulations of localized rainstorms in sub-Saharan Africa produced using massive, crowd-sourced computing power from World Community Grid.
Keywords: Africa, rainfall, precipitation, modeling
Conventions: CF 1.8
Projection: Lambert Conformal
Source: Weather Research and Forecasting (WRF) Model V3.9.1.1 run on the IBM World Community Grid (WCG)
Processing Level:
License: This work is licensed under ___.

CF-1.8 Convention
^^^^^^^^^^^^^^^^^
http://cfconventions.org/Data/cf-conventions/cf-conventions-1.8/cf-conventions.htm

Viewing file metdata with ncdump from NCO
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The pre-processed dataset available via THREDDS is stored in the netCDF3 64-bit offset data model, in the netCDF3 file format. The metadata for files that have been downloaded from this server can be found using multiple tools specific for working with netCDF files. One recommended tool for viewing this metadata and working with netCDF files in general is a set of command line programs called the NetCDF Operators (NCO). These can be downloaded from http://nco.sourceforge.net/ and installed following instructions on that page.

Once you have the NCO programs installed, you can use the ncdump command to view the metadata for any netCDF file.

`$ ncdump -h filename.nc`

For more options when using ncdump, see `this webpage <https://www.unidata.ucar.edu/software/netcdf/workshops/2011/utilities/NcdumpExamples.html>`_`.

You should see an output in your terminal with the following information:

dimensions:
   time =
   lat =
   lon =
   DateStrLen = 19

variables:

// global attributes:
   :title =
   :summary =
   :keywords =
   :Conventions = "CF-1.8"
   :naming_authority = "nl.tudelft"
   :source = "WRF-V3.9.1.1"
   :processing_level = "These data were processed from their original form. For more details, see ___"
   :license =
   :data_created =
   :creator_name =
   :institution = "TU Delft"
   :project = "Africa Rainfall"
   :contributor_names = ''
   :projection = 'Lambert Conformal'
   :geospatial_bounds =
   :geospatial_bounds_crs =
   :geospatial_bounds_vertical_crs = ''
   :geospatial_lat_min = " " ;
	 :geospatial_lat_max = " " ;
   :geospatial_lat_units = 'degrees_north'
   :geospatial_lat_resolution = ''
	 :geospatial_lon_min = " " ;
	 :geospatial_lon_max = " " ;
   :geospatial_lon_units = 'degrees_east'
   :geospatial_lon_resolution = ''
   :geospatial_vertical_min = ''
   :geospatial_vertical_max = ''
   :time_coverage_start = ''
   :time_coverage_end = ''
   :time_coverage_duration = ''
   :time_coverage_resolution = ''
	 :cdm_data_type = "Grid" ;
   :metadata_link = ''
	 :references = "Link to documentation" ;
