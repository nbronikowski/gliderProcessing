## name list
#
# Note: when no variable name available in this list fill the variable names with the
# variable name and empty units and empty comment
#
# The variables have to comply with CF conventions where applicable
# \href{https://cfconventions.org/Data/cf-standard-names/current/build/cf-standard-name-table.html|}
#
# FORMAT USED FOR NAMING VARIABLES
#	standard_variable_name		,		long_name		,		units		,		comments



# Main variables
"time"							,	"time"																			,	"s"						,	"glider time record seconds since 1970. Time is merged time between glider flight and science computers"
"pressure"					,	"sea_water_pressure"													,	"dbar"					,	"measured by glider CTD pressure sensor"
"depth"							,	"depth"																			,	"meter"					,	"vertical distance below sea surface calculated from CTD pressure sensor sci_water_pressure"
"longitude"					,	"longitude"																	,	"degree_east"		,	"glider platform longitude (when possible) incorporating underwater positioning corrected for dead reckoninig errors associated with underwater currents and glider GPS surface positions"
"latitude"						,	"latitude"																		,	"degree_north"		,	"glider platform latitude (when possible) incorporating underwater positioning corrected for dead reckoninig errors associated with underwater currents and glider GPS surface positions"
"profile_index"				,	"glider_dive_profile_index",											,	" "							,	"profile index computed from glider CTD depth to extract profiles for identifying valid profiles in the glider record, based on the SOCIB toolbox. The output has integers for valid profiles (dive or climb) and fractions denote in-between dive states or hovering states"
"profile_direction"			,	"glider_dive_profile_direction"										,	" "							,	"profile direction indicating dive (-1) or climb (+1)"
"northward_sea_water_velocity" , "northward_sea_water_velocity"					,	"m s-1"					,	"measured depth-average of sea water velocity pointing positive North, computed as an average over a glider dive segement between surfacing locations. The value comes from m_water_final_vy"
"eastward_sea_water_velocity" , "eastward_sea_water_velocity"						,	"m s-1"					,	"measured depth-average of sea water velocity pointing positive East, computed as an average over a glider dive segement between surfacing locations. The value comes from m_water_final_vx"
"conductivity"				,	"sea_water_electrical_conductivity"							,	"S m-1"				,	"ambient seawater conductivity measured by glider CTD sensor sci_water_cond"
"temperature"				,	"sea_water_temperature"											,	"degree_C"			,	"ambient seawater temperature measured by glider CTD sensor sci_water_temp"
"salinity"						,	"sea_water_practical_salinity"										,	"PSU"					,	"practical salinity computed from conductivity, temperature and pressure using the Gibbs-SeaWater (GSW) Oceanographic toolbox {https://www.teos-10.org/software.htm}"
"density"						,	"sea_water_density"													,	"kg m-3"				,	"in-situ seawater density calculated from absolute salinity, conservative temperature and pressure using the Gibbs-SeaWater (GSW) Oceanographic toolbox {https://www.teos-10.org/software.htm}"
"absolute_salinity"		,	"sea_water_absolute_salinity"										,	"g kg-1"				,	"in-situ seawater absolute salinity calculated from practical salinity, conservative temperature and pressure using the Gibbs-SeaWater (GSW) Oceanographic toolbox {https://www.teos-10.org/software.htm}"
"conservative_temperature"	,	"sea_water_conservative_temperature"			,	"degree_C"				,	"in-situ seawater conservative temperature calculated from practical salinity, conservative temperature and pressure using the Gibbs-SeaWater (GSW) Oceanographic toolbox {https://www.teos-10.org/software.htm}"
"oxygen_sensor_temperature"	,	"temperature_of_sensor_for_oxygen_in_sea_water"	,	"degree_C"	, "temperature of oxygen sensor used to compute oxygen concentration duplicated from sci_oxy4_temperature"
"oxygen_concentration"				,	"mole_concentration_of_dissolved_molecular_oxygen_in_sea_water"	,	"micro-mol L",	"oxygen concentration measured by glider sensor from sci_oxy4_oxygen, compensated for salinity using code from Henry Bittig."


# GLIDER FLIGHT COMPUTER VARIABLES
"c_ballast_pumped"		,	"commanded_glider_ballast_pumped"						,	"cm3"						,	"-negative is subtraction / + addition"
"c_battpos"					,	"commanded_glider_pitch_battery_position"				,	"in"							,	"-negative is towards aft and +positive is towards nose"
"c_de_oil_volume"		,	"commanded_glider_oil_ballast_pumped"					,	"cm3"						,	"-negative is subtraction / + addition"
"c_fin"							,	"commanded_glider_rudder_angle"							,	"degree"					,	"-negative is port / + starboard"
"m_fin"							,	"measured_glider_roll"												,	"degree"					,	"-negative is port / + starboard"
"c_heading"					,	"commanded_glider_heading_angle"							,	"degree"					,	"-negative is port / + starboard"
"c_pitch"						,	"commanded_glider_pitch_angle"								,	"degree"					,	"-negative is nose down / + is up"
"c_wpt_lat"					,	"commanded_glider_target_waypoint_latitude"			,	"degree_north"			,	"decimal degrees North WGS84 (+90/-90)"
"c_wpt_lon"					,	"commanded_glider_target_waypoint_longitude"		,	"degree_east"			,	"decimal degrees East WGS84 (+180/-180)"
"m_ballast_pumped"	,	"measured_glider_ballast_pumped"							,	"cm3"						,	"-negative is subtraction / + addition"
"m_battpos"					,	"measured_glider_pitch_battery_position"					,	"in"							,	"-negative is towards aft and +positive is towards nose"
"m_de_oil_volume"		,	"measured_glider_oil_ballast_pumped"						,	"cm3"						,	"-negative is subtraction / + addition"
"m_fin"							,	"measured_glider_rudder_angle"								,	"degree"					,	"-negative is port / + starboard"
"m_heading"				,	"measured_glider_heading_angle"								,	"degree"					,	"-negative is port / + starboard"
"m_pitch"						,	"measured_glider_pitch_angle"									,	"degree"					,	"-negative is nose down / + is up"
"m_altitude"					,	"measured_glider_altitude_above_bottom"					,	"meter"						,	"   "
"m_battery"					,	"measured_glider_main_battery_voltage"					,	"volts"						,	"	"
"m_pressure"				,	"measured_glider_pressured_sensor_reading"			,	"bar"							,	"measured by glider aft-cap MICRON pressure transducer"
"m_depth"					,	"measured_glider_depth_readings"							,	"meter"						,	"depth is computed from m_pressure"
"m_water_depth"			,	"measured_glider_water_depth"									,	"meter"						,	"depth is computed from adding m_depth+m_altitude"
"m_gps_lat"					,	"measured_glider_gps_latitude"									,	"degree_north"			,	"decimal degrees North WGS84 (+90/-90), recorded by glider at surface"
"m_gps_lon"				,	"measured_glider_gps_longitude"								,	"degree_east"			,	"decimal degrees East WGS84 (+180/-180), recorded by glider at surface"
"m_lat"							,	"measured_glider_dead_reckoned_latitude"				,	"degree_north"			,	"decimal degrees North WGS84 (+90/-90), recorded using glider compass"
"m_lon"						,	"measured_glider_dead_reckoned_longitude"			,	"degree_east"			,	"decimal degrees East WGS84 (+180/-180), recorded using glider compass"
"m_water_vy"				,	"measured_glider_northward_water_velocity"			,	"m s-1"						,	" "
"m_water_vx"				,	"measured_glider_eastward_water_velocity"				,	"m s-1"						,	" "
"m_final_water_vy"		,	"measured_final_glider_northward_water_velocity"	,	"m s-1"						,	" "
"m_final_water_vx"		,	"measured_final_glider_eastward_water_velocity"		,	"m s-1"						,	" "
"m_initial_water_vy"	,	"measured_initial_glider_northward_water_velocity"	,	"m s-1"						,	" "
"m_initial_water_vx"	,	"measured_initial_glider_eastward_water_velocity"	,	"m s-1"						,	" "
"x_dr_state"					,	"estimated_glider_dead_reckoning_state"					,	"enum"						,	"this variable contains the glider states (surfacing=2, about to surface=1, about to dive =3, diving=4) which can be used to parse apart the glider gps locations for dead-reckoning error estimation and correction of the measured glider compass underwater positions."
"m_present_time"		,	"measured_glider_flight_computer_time"					 ,	"s"				,	"seconds since 1970, epoch time stamp on glider flight computer for all glider flight computer variables and sensors"


# GLIDER SCIENCE COMPUTER VARIABLES
"sci_m_present_time"			,	"science_measured_glider_science_computer_time"					 ,	"s"						,	"seconds since 1970, epoch time stamp on glider science computer for all glider science variables and sensors"
"sci_m_science_on"			,	"science_measured_glider_science_computer_state"				,	"enum"					,	"off=0, on=1"
"sci_water_cond"					,	"science_measured_sea_water_electrical_conductivity"			,	"S m-1"				,	"  "
"sci_water_pressure"			,	"science_measured_sea_water_pressure"									,	"dbar"					,	"  "
"sci_water_temp"					,	"science_measured_sea_water_temperature"							,	"degree_C"			,	"  "
"sci_water_salninty"				, 	"science_computed_sea_water_practical_salinity"						,	"PSU"					, 	"from sci_water_temp, sci_water_cond, sci_water_pressure"

# RBR CTD
"sci_rbrctd_cond_cell_temp_00",	"rbr_ctd_temperature_of_conductivity_cell",	"degree_C"			,	"internal temperature of the RBR conductivity cell used for correcting salinity and temperature in post-processing"
"sci_rbrctd_conductivity_00"		,	"rbr_ctd_conductivity_of_conductivity_cell"	,	"S m-1"				,	"conductivity of the RBR conductivity cell used for correcting salinity and temperature in post-processing"
"sci_rbrctd_temperature_00"		,	"rbr_ctd_thermistor_temperature"				,	"degree_C"			,	"temperature readings of the external RBR thermistor measuring ambient seawater temperature"
"sci_rbrctd_seapressure_00"		,	"rbr_ctd_sea_water_pressure"					,	"dbar"					,	"used in sci_water_pressure"
"sci_rbrctd_salinity_00"				,	"rbr_ctd_computed_practical_salinity"			,	"PSU"					,	"salinity computed by RBR CTD from temperature, pressure and conductivity"


# Oxygen Optode
"sci_oxy4_calphase"					,	"oxygen_optode_calibrated_phase_readings" , "degree"			,	"temperature calibrated and compensated phase angle output of the oxygen optode used in the 7 foil coeffiecients SVU Formula Uchida et al. (2008) to compute oxygen.
"sci_oxy4_tcphase"						,	"oxygen_optode_temperature_compensated_phase_readings",	"degree",		"temperature compensated phase angle output of the oxygen optode. Input is used in the 4x7 coefficient oxygen foil model to compute the oxygen concentration from temperature and tcphase.
"sci_oxy4_oxygen"						,	"oxygen_optode_molar_oxygen_concentration"							,	"micro-mol L"	,	"oxygen concentration of the glider optode sensor computed internally from sci_oxy4_calphase and sci_oxy4_temp but not compensated for varying salinity. Salinity is set internaly to S=0 PSU"
"sci_oxy4_temp"							,	"oxygen_optode_temperature"													,	"degree_C"		,	"oxygen sensor thermistor readings"
"sci_oxy4_saturation"					,	"oxygen_optode_sea_water_saturation"										,	"1"					,	"oxygen sensor seawater saturation computed internally from thermistor readings sci_oxy4_temp using forumlae from Benson and Krause (1984), as fitted by Garcia and Gordon (1992, 1993), but not accounting for salinity"



