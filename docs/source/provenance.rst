Production of raw data files
============================
**Data available for download have been processed from their original raw form.** This page describes the generation of the raw simulation data, including which model and parameter values were used to generate it. Steps taken to produce the processed data are described in the "Data pre-processing" section of this site.

Raw data production
-------------------
Data are high-resolution computer simulations of localized rainstorms in sub-Saharan Africa produced using massive, crowd-sourced computing power from World Community Grid.

World Community Grid volunteer program
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
World Community Grid volunteers download a secure software program to their computer. When the computer is idle or not using its full computing power, it will run a simulated experiment in the background. Then, the computer contacts the World Community Grid server to let it know that it has completed the simulation, which is then uploaded to an IBM server. All of this happens unobtrusively.

World Community Grid receives the results volunteers send back (often called work units or research tasks), combines them with hundreds of thousands of results from other volunteers all over the world, and sends them to the Delft research team. The researchers then begin the difficult work of analyzing the data. While this process can take years, it accelerates that would otherwise take decades, or might even be impossible.

The amount of data produced is about 0.5 PB or, in more nostalgic terms, a pile of floppy disks of over 1000 km. That pile would weigh over 6700 tons and would be over 1200 km high. About twenty variables of direct interest are stored and uploaded to the central WCG facility. These data are stored in netCDF files.

Model architecture
------------------
The model used to produce these simulations is the Weather Research and Forecasting Model (WRF) V3.9.1.1 from the National Center for Atmospheric Research (NCAR). The WRF is “a next-generation mesoscale numerical weather prediction system designed for both atmospheric research and operational forecasting applications.” For the African Rainfall project, the WRF produces simulations based on actual atmospheric conditions.

ARP divides the African continent into over 35609 WRF modelling domains. For each domain of 50x50 cells, WRF is run on a personal computer of a volunteer, who shares spare computing resources via the WCG. It calculates episodes of two days’ worth of weather with output for every 15 minutes (193 total time steps each).

Each WRF domain is triply nested.  Hence, it first calculates at a coarse resolution of 9km x 9km covering a  468km x 468km region with historical boundary conditions from NOAA's Global Forecast System (GFS-ANL).  Within the center of this domain, it calculates the next domain at the intermediate resolution of 3 km (156 km x 156 km) with the boundary conditions set by the coarser domain calculation. Finally, a domain of 52 km x 52km is calculated at the center of the intermediate domain. Vertically, the atmosphere is divided into 51 layers so that the output is produced on a 52x52x51 grid.

Model input parameter values
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The following parameter values were used as inputs for the WRF model in order to produce the resulting simulation data.

===============================  ========================  ===================================================================================================================================================
PARAMETER                        VALUE                     DESCRIPTION
===============================  ========================  ===================================================================================================================================================
SIMULATION START DATE            2018-07-01_00:00:00       The date and time when the simulation commenced.
WEST-EAST_GRID_DIMENSION         52                        Dimension of the grid in the West-East direction.
SOUTH-NORTH_GRID_DIMENSION       52                        Dimension of the grid in the South-North direction.
BOTTOM-TOP_GRID_DIMENSION        51                        Dimension of the grid in the vertical direction.
DX                               9000.f                    Grid resolution in the X direction (m).
DY                               9000.f                    Grid resolution in the Y direction (m).
SKEBS_ON                         0                         Stochastic kinetic energy backskatter scheme.
SPEC_BDY_FINAL_MU                1                         Whether to call spec_bdy_final for mu.
USE_Q_DIABATIC                   0                         Whether to include QV and QC tendencies in advection (i.e. to consider moisture tendency from microphysics in small steps).
GRIDTYPE                         C                         Type of grid used by the model.
DIFF_OPT                         1                         Turbulence and mixing option.
KM_OPT                           4                         Eddy coefficient option.
DAMP_OPT                         0                         Upper-level damping flag (0 = no damping).
DAMP_COEFF                       0.2f                      Damping coefficient.
KHDIF                            0.f                       Horizontal diffusion constant (m2/s).
KVDIF                            0.f                       Vertical diffusion constant (m2/s).
MP_PHYSICS                       10                        Microphysics scheme.
RA_LW_PHYSICS                    4                         Longwave radiation scheme.
RA_SW_PHYSICS                    4                         Shortwave radiation scheme.
SF_SFCLAY_PHYSICS                2                         Surface layer scheme.
SF_SURFACE_PHYSICS               2                         Land surface scheme.
BL_PBL_PHYSICS                   2                         Planetary boundary for layer scheme.
CU_PHYSICS                       3                         Cumulus parameterization scheme.
SF_LAKE_PHYSICS                  0                         Lake physics scheme.
SURFACE_INPUT_SOURCE             3                         Landuse and soil category.
SST_UPDATE                       1                         Option to use time-varying SST, seaice, vegetation fraction, and albedo during a model simulation.
GRID_FDDA                        0                         Grid nudging option (0 = none).
GFDDA_INTERVAL_M                 0                         Time interval (minutes) vetween analyses for the grid nudging.
GFDDA_END_H                      0                         Time (hours) to stop nudging after the start of the forecast.
GRID_SFDDA                       0                         Surface FDDA switch (0 = off).
SGFDDA_INTERVAL_M                0                         Time interval (minutes) between surface analsysis times.
SGFDDA_END_H                     0                         Time (hours) to stop surface nudging after start of the forecast.
HYPSOMETRIC_OPT                  2                         Hypsometric option.
USE_THETA_M                      0                         Whether to use theta (1+1.61QV).
GWD_OPT                          0                         Gravity wave drag option (0 = off).
SF_URBAN_PHYSICS                 1                         Urban surface model option.
SF_OCEAN_PHYSICS                 0                         Ocean model option.
SHCU_PHYSICS                     0                         Shallow convection option.
MFSHCONV                         0                         Turns on day-time EDMF for QNSE (0 = off).
FEEDBACK                         0                         For nested domain: 0 = one-way nesting, 1 = two-way nesting.
SMOOTH_OPTION                    2                         Smoothing option for the parent domain in the area of the nest if feedback is on.
SWRAD_SCAT                       1.f                       Scattering turning parameter for ra_sw_physics = 1.
W_DAMPING                        1                         Vertical velocity damping flag.
DT                               36.f                      Time step (seconds).
RADT                             1.f                       Minutes between radiation physics calls.
BLDT                             0.f                       Minutes between boundary-layer physics calls (0 = call every time step).
CUDT                             0.f                       Minutes between cumulus physics calls.
AER_OPT                          0                         Aerosol input option (RRTMG only).
SWINT_OPT                        0                         Interpolation of shortwave radiation based on the updated solar zenith angle between radiation calls (0 = no interpolation, 1 = use interpolation)
AER_TYPE                         1                         Aerosol type to be used
AER_A0D550_OPT                   1                         \
AER_ANGEXP_OPT                   1                         \
AER_SSA_OPT                      1                         \
AER_ASY_OPT                      1                         \
AER_AOD550_VAL                   0.12f                     \
AER_ANGEXP_VAL                   1.3f                      \
AER_SSA_VAL                      0.85f                     \
AER_ASY_VAL                      0.9f                      \
MOIST_ADV_OPT                    1                         Advection options for moisture.
SCALAR_ADV_OPT                   1                         Advection options for scalars.
TKE_ADV_OPT                      1                         Advection options for TKE.
DIFF_6TH_OPT                     0                         6th-order numerical diffusion (0 = none).
DIFF_6TH_FACTOR                  0.12f                     6th-order numerical diffusion non-dimensional rate.
OBS_NUDGE_OPT                    0                         obs-nudging fdda (0 = off).
BUCKET_MM                        -1.f                      Bucket reset values for water accumulation (-1 = inactive).
BUCKET_J                         -1.f                      Bucket reset value for energy accumulations (-1 = inactive).
PREC_ACC_DT                      0.f                       Bucket reset time interval between outputs for cumulus or grid-scale precipitation (in minutes).
ISFTCFLX                         0                         Alternative Ck (exchange coefficient for temp and moisture), Cd (drag coefficient for momentum) formulation for tropical storm application.
ISHALLOW                         0                         Turns on shallow convection (default is 0 = off).
ISFFLX                           1                         Heat and moisture fluxes from the surface for real-data cases and when a PBL is used.
ICLOUD                           1                         Cloud effect to the optical depth in radiation.
ICLOUD_CU                        0                         \
TRACER_PBLMIX                    1                         Mix tracer fields consistent with PBL option.
SCALAR_PBLMIX                    0                         Mix scalar fields consistent with PBL option.
YSU_TOPDOWN_PBLMIX               0                         Turns on top-down radiation-driven mixing (default is 0 = no).
GRAV_SETTLING                    0                         Gravitational settling of fog/cloud droplets (default 0 = no settling).
DFI_OPT                          0                         Digital filter initialization (default 0 = none).
SIMULATION_INITIALIZATION_TYPE   REAL DATA CASE            \
WEST-EAST_PATCH_START_UNSTAG     1                         \
WEST-EAST_PATCH_END_UNSTAG       51                        \
WEST-EAST_PATCH_START_STAG       1                         \
WEST-EAST_PATCH_END_STAG         52                        \
SOUTH-NORTH_PATCH_START_UNSTAG   1                         \
SOUTH-NORTH_PATCH_END_UNSTAG     51                        \
SOUTH-NORTH_PATCH_START_STAG     1                         \
SOUTH-NORTH_PATCH_END_STAG       52                        \
BOTTOM-TOP_PATCH_START_UNSTAG    1                         \
BOTTOM-TOP_PATCH_END_UNSTAG      50                        \
BOTTOM-TOP_PATCH_START_STAG      1                         \
BOTTOM-TOP_PATCH_END_STAG        51                        \
GRID_ID                          1                         Domain identifier (can be 1, 2 or 3).
PARENT_ID                        0                         ID of the parent domain.
I_PARENT_START                   1                         The starting lower-left corner i-indice from the parent domain.
J_PARENT_START                   1                         The starting lower-left corner j_indice from the parent domain.
PARENT_GRID_RATIO                1                         Parent-to-nest domain grid size ratio.
CEN_LAT                          12.99997f                 Latitude of the domain's center.
CEN_LON                          -4.950012f                Longitude of the domain's center.
TRUELAT1                         20.f                      Projection parameter - true latitude 1.
TRUELAT2                         0.f                       Projection parameter - true latitude 2.
MOAD_CEN_LAT                     12.99997f                 Mother of all domains center latitude.
STAND_LON                        5.f                       Projection parameter - standard longitude.
POLE_LAT                         90.f                      The pole latitude.
POLE_LON                         0.f                       The pole longitude.
GMT                              0.f                       \
JULYR                            2018                      \
JULDAY                           182                       \
MAP_PROJ                         1                         Map projection.
MAP_PROJ_CHAR                    Lambert Conformal         Map projection.
MMINLU                           MODIFIED_IGBP_MODIS_NOAH  Related to land use category.
NUM_LAND_CAT                     21                        Number of land categories in input data.
ISWATER                          17                        Related to land use category.
ISLAKE                           21                        Related to land use category.
ISICE                            15                        Related to land use category.
ISURBAN                          13                        Related to land use category.
ISOILWATER                       14                        Related to land use category.
HYBRID_OPT                       -1                        Option related to the hybrid vertical coordinates.
ETAC                             0.f                       Option related to the hybrid vertical coordinates.
===============================  ========================  ===================================================================================================================================================

Time period
-----------
The period of simulation data covered runs from 1 June 2018 until 31 May 2019. Raw simulation data are generated at a 15-minute time interval. Approximately 40% of total expected data have been created, if this pace continues the dataset will be complete in mid-2022.

Units
-----
Units define geographic areas for which simulations results are available or will be available. A total of 35.609 square units cover Sub-Saharan Africa.
For each unit, simulation results are produced at three spatial granularities called domains. Thus, a domain can also be described as a subset of a unit with a particular spatial resolution.

The domains used in the simulation have the following resolutions:

+ Domain 1: 9 km
+ Domain 2: 3 km
+ Domain 3: 1 km

The centroid of each unit is separated by 15.3 minutes of arc in both latitude and longitude. Each unit partially overlaps with adjacent units; all domains contain 51 X 51 grid points. The model results are non-deterministic, so units were designed to overlap and create redundancy for a given geographic location, i.e., more than one value for an specific geographic location at a given time. These values were treated in the processed data available for download, to remove the overlapping values effect. More information about how this was done can be found in the "Data processing" section.

Georeferencing information
--------------------------

The projection of the raw data is Lambert Conformal with the true latitudes 1 and 2 being 20 and 0 degrees, respectively. The standard longitude is 5 degrees.

Variables in raw dataset
------------------------

=============  ====================================================================================  =============  =============  ===============
VARIABLE       DESCRIPTION                                                                           DATA TYPE      UNITS          GEOGRAPHIC DATA
=============  ====================================================================================  =============  =============  ===============
Times          --                                                                                    char           --             No
HFX_FORCE      SCM ideal surface sensible heat flux                                                  float          W/m2           No
NEST_POS       --                                                                                    float          --             Yes
Q2             Water vapor mixing ratio (QV) at 2m                                                   float          Kg/Kg          Yes
T2             Air temperature at 2m                                                                 float          K              Yes
TH2            Potential temperature at 2m                                                           float          K              Yes
PSFC           Surface air pressure                                                                  float          Pa             Yes
U10            U component of the wind speed at 10m (X surface wind)                                 float          m/s            Yes
V10            V component of the wind speed at 10 m (Y surface wind)                                float          m/s            Yes
ITIMESTEP      --                                                                                    int            --             No
XTIME          Minutes since 2018-07-01 00:00:00                                                     float          minutes        No
SMOIS          Soil moisture                                                                         float          m3/m3          Yes
P_TOP          Pressure top of the model                                                             float          Pa             No
RAINC          Accumulated total cumulus precipitation (convective precipitation)                    float          mm             Yes
RAINSH         Accumulated shallow cumulus precipitation (large-scale precipitation)                 float          mm             Yes
RAINNC         Accumulated total grid scale precipitation (non-convective precipitation)             float          mm             Yes
SWDOWN         Downward short wave flux at ground surface (surface downwelling shortwave radiation)  float          W/m2           Yes
GLW            Downward long wave flux at ground surface (surface downwelling longwave radiation)    float          W/m2           Yes
OLR            Top of atmosphere outgoing longwave radiation                                         float    W/m2    Yes
SR             Fraction of frozen precipitation                                                      float          --             Yes
SST            Sea surface temperature                                                               float          K              Yes
=============  ====================================================================================  =============  =============  ===============
