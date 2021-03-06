.. caracal documentation master file, created by
   sphinx-quickstart on Mon Feb 18 15:04:26 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.
 
.. _obsconf:
 
==========================================
obsconf
==========================================
 
.. toctree::
   :maxdepth: 1
 
Set up some basic information about the observation(s).



.. _obsconf_obsinfo:

--------------------------------------------------
**obsinfo**
--------------------------------------------------

  Get observation information.

  **enable**

    *bool*

    Execute the obsconf worker.

  **listobs**

    *bool*, *optional*, *default = True*

    Run the CASA 'listobs' task to get observation information.

  **summary_json**

    *bool*, *optional*, *default = True*

    Run the MSUtils summary function to get observation information written as a JSON file, which can then be used to automatically configure pipeline.

  **vampirisms**

    *bool*, *optional*, *default = False*

    Return the time range over which observations were taken at night.

  **plot_elevation_tracks**

    Make Elevation vs Hour-angle plots for observed fields.

    **enable**

      *bool*, *optional*, *default = True*

      Enable segment 'plot_elevation_tracks'.

    **plotter**

      *{"plotms", "owlcat"}*, *optional*, *default = owlcat*

      The application to be used for making plots. Options are 'plotms' and 'owlcat'.



.. _obsconf_target:

--------------------------------------------------
**target**
--------------------------------------------------

  *list* *of str*, *optional*, *default = all*

  The field name(s) of the target field(s), separated by commas if there are multiple target fields. Or set this parameter to 'all' to select all of the target fields.



.. _obsconf_gcal:

--------------------------------------------------
**gcal**
--------------------------------------------------

  *list* *of str*, *optional*, *default = all*

  The field name(s) of the gain (amplitude/phase) calibrator field(s). Or set 'all' to select all of the gcal fields, 'longest' to select the gcal field observed for the longest time, or 'nearest' to select the gcal field closest to the target. Note that if multiple targets and gcals are present, then 'all' (for both the 'target' and 'gcal' parameters) means that each target will be paired with the closest gcal.



.. _obsconf_bpcal:

--------------------------------------------------
**bpcal**
--------------------------------------------------

  *list* *of str*, *optional*, *default = longest*

  The field name(s) of the bandpass calibrator field(s). Or set 'all' to select all of the bpcal fields, 'longest' to select the bpcal field observed for the longest time, or 'nearest' to select the bpcal field closest to the target.



.. _obsconf_fcal:

--------------------------------------------------
**fcal**
--------------------------------------------------

  *list* *of str*, *optional*, *default = longest*

  The field name(s) of the fluxscale calibrator field(s). Or set 'all' to select all of the fcal fields, 'longest' to select the fcal field observed for the longest time, or 'nearest' to select the fcal field closest to the target.



.. _obsconf_xcal:

--------------------------------------------------
**xcal**
--------------------------------------------------

  *list* *of str*, *optional*, *default = longest*

  The field name(s) of the crosshand phase-angle calibrator field(s). Or set 'all' to select all of the xcal fields, 'longest' to select the xcal field observed for the longest time, or 'nearest' to select the xcal field closest to the target. This calibrator must be linearly polarized and have a non-zero parallactic angle coverage at the time of observation in order to solve for the X-Y offsets in digitizers and the absolute polarization angle of the system. Successful calibration derotates U from V.



.. _obsconf_reference_antenna:

--------------------------------------------------
**reference_antenna**
--------------------------------------------------

  *str*

  The reference antenna, which can be identified by an antenna name or number.



.. _obsconf_report:

--------------------------------------------------
**report**
--------------------------------------------------

  *bool*, *optional*, *default = False*

  (Re)generate a full HTML report at the end of this segment.

