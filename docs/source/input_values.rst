Model input parameter values
============================

Simulation datasets were produced using the following parameters for the WRF model:

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
SGFDDA_INTERVAL_M                0                         Time interval (minutes) between surface analysis times.
SGFDDA_END_H                     0                         Time (hours) to stop surface nudging after the start of the forecast.
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
