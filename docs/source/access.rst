Accessing ARP data
==================

THREDDS server
--------------
Data are stored as netCDF files (netCDF 3 classic 64-bit) on a THREDDS server hosted at TU Delft. To access these data over the OPeNDAP protocol, use this URL: http://africarain.ceg.tudelft.nl:8080/thredds/catalog.html

To work with these files on your local system via OPeNDAP, you first need to obtain an OPeNDAP-enabled client program. Some common client programs include NCO, MATLAB, R, ArcGIS, Python and others. Please see this `information page <https://psl.noaa.gov/data/gridded/using_dods.html>`_ from the NOAA Physical Sciences Library for more information.

--------------

.. code-block:: python

   import netCDF4

   # endpoint for specfic file

   url = 'https://africarain.ceg.tudelft.nl:9010/thredds/dodsC/demos/demo.nc'

   # read dataset
   nc = netCDF4.Dataset(url)

   # read variables
   ncv = nc.variables
   print(ncv.keys())

   # # subset and subsample
   # lon = ncv['longitude'][10:-10:2,20:-10:2]
   # lat = ncv['latitude'][10:-10:2,20:-10:2]

   # read the nth time step
   itime = 10
   tair = ncv['air_temperature'][itime]

   print(tair)

   # pcolormesh(lon,lat,tair);
   # colorbar();

   '''
   Other examples: https://publicwiki.deltares.nl/display/OET/Reading+data+from+OpenDAP+using+python
   '''

   #  other thredds server: http://dapds00.nci.org.au/thredds/catalog.html

----------

Contact
-------
Processed data are available directly from the THREDDS URL listed above. Data must be cited appropriately and used in accordance with licensing requirements (see `Licensing and citation <https://africarain.readthedocs.io/en/latest/citing.html>`_).

Raw data files (see `Production of raw data files <https://africarain.readthedocs.io/en/latest/provenance.html#production-of-raw-data-files>`_) are available upon request from Nick van de Giesen, n.c.vandegiesen@tudelft.nl.
