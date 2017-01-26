# sorghum-energy-crop-model
## Energy-sorghum_crop-model_VPD-limited_transpiration
XML files reflective of a bioenergy sorghum plant that can be evaluated in APSIM and C++ code for a VPD limited-transpiration trait in the sorghum module of APSIM. 
### Dependencies: 
  - APSIM version 7.7 [http://www.apsim.info/](http://www.apsim.info/); described in [Holzworth et al. (2014)](http://dx.doi.org/10.1016/j.envsoft.2014.07.009).

### Usage:
1. To evaluate the energy sorghum plant within vanilla APSIM framework use the XML files provided (energy\_sorghum\_template.xml and energy\_sorghum\_template.apsim) with Meteroloical file (cs\_dos.met)* and continue in APSIM.

2. To evaluate energy sorghum for its VPD-limited transpiration trait,
	1. must use APSIM from source code, follow instructions on developer site: [Building APSIM from source](https://www.apsim.info/Documentation/TechnicalandDevelopment/BuildingAPSIMfromsource.aspx)  
	2. replace .cpp and .h files provided in the VPD-limited\_transpiration folder in the Sorghum module within APSIM ("../trunk/Model/Sorghum/")
	3. build APSIM from source with VPD-limited transpiration modifications
	4. construct XML files with VPD-limited transpiration parameters and agronomic cropping parameters* either directly in the XML files (energy\_sorghum\_template.xml and energy\_sorghum\_template.apsim) or iteratively through a bash shell (construct\_APSIM-Esb\_VPD-LT.sh).
		* VPD breakpoint
		* m1
		* m2
	5. simulate crop growth by editing path and then running run\_vpd\_limited-transpiration\_simulations.sh
*Meteroligical file for College Station, TX, 2000-2014 and 2020 (2008 data with no rainfall) is contained in cs\_dos.met

### More information:
This crop model and evaluation of VPD-limited transpiration in energy sorghum is part of the Supplemental Materials from [Truong, McCormick, & Mullet (submitted, 2016)](). If you have any further questions, please contact Sandra K. Truong <thkhavi@tamu.edu>.


