Accessing ARP data
==================

THREDDS server
--------------
Data are stored as netCDF files (netCDF 3 classic 64-bit) on a THREDDS server hosted at TU Delft. These data can be accessed for anlysis purpose, using the OPeNDAP protocol. The main data catalog is available at: https://africarain.ceg.tudelft.nl:9010/thredds/catalog.html

To work with these files on your local system via OPeNDAP, you first need to obtain an OPeNDAP-enabled client program. Some common client programs include NCO, MATLAB, R, ArcGIS, Python and others. Please see this `information page <https://psl.noaa.gov/data/gridded/using_dods.html>`_ from the NOAA Physical Sciences Library for more information.

--------------

Access ARP data using Python
----------------------------

This is an example of how to access data from the Africa Rain THREDDS server using Python. This relies on the netCDF4 library, a powerful library for working with netCDF data in general. This example uses a dummy dataset, which endpoint is ``https://africarain.ceg.tudelft.nl:9010/thredds/dodsC/demos/demo.nc``

.. code-block:: python

   import netCDF4

   # endpoint for specific file

   url = 'https://africarain.ceg.tudelft.nl:9010/thredds/dodsC/demos/demo.nc'

   # read dataset
   nc = netCDF4.Dataset(url)

   # read variables
   ncv = nc.variables
   print(ncv.keys())

   ## a subset of the data set can be retrieved using coordinate.
   ## Use relevant coordinates for your dataset, the values below are just an example
   # lon = ncv['longitude'][10:-10:2,20:-10:2]
   # lat = ncv['latitude'][10:-10:2,20:-10:2]

   # read the nth time step
   itime = 10
   tair = ncv['air_temperature'][itime]

   # print data
   print(tair)

   ## Other examples: https://publicwiki.deltares.nl/display/OET/Reading+data+from+OpenDAP+using+python
   


----------

Contact
-------

Processed data will be available directly from the THREDDS URL listed above. Data must be cited appropriately and used in accordance with licensing requirements. See :doc:`/citing`

Raw data files (see :doc:`provenance`) are available upon request from Nick van de Giesen, n.c.vandegiesen@tudelft.nl.
