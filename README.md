This is the code used to process streamflow (discharge), precipitation, evapotranspiration and soil moisture data for the manuscript entitled: 
"Land use and drought effects on groundwater outflow in headwater catchment water balances in the southeastern Amazon"

We assessed the total water balance of forested and agriculturally dominated catchments during normal and drought years using the following equation (Eq. 1): 
P= ET+Q+dS/dt+Goutflow  

where P=precipitation, ET= evapotranspiration, Q=discharge and dS/dt = change in subsurface storage (dS) over time (dt), and Goutflow=groundwater outflow. Below is a brief description of the datasets used to estimate each component of the water balance used in the code in the repository. 

Precipitation (P):  Monthly mean precipitation was extracted from each selected land-use pixel using the Climate Hazards Group InfraRed Precipitation with Station data (CHIRPS) for the study period. The drought year (2016) was driven by a strong El Nino-Southern Oscillation event that brought record-breaking heat and extreme drought across the Amazon Basin.

Evapotranspiration (ET): To estimate spatial-temporal variations in evapotranspiration (ET) for the land uses in our study watersheds, we used the MODIS ET time series (MOD16A2, v6.2), available every 8 days at 500-m resolution from 2000-2022 (Running et al., 2021). To do so, we created a grid of “pure pixels” (i.e., that were solely in one land use and sufficiently distant from edges to avoid mixed signals or edge effects; see Figure 1) and extracted ET data for 80 1-km2 pixels in forest and cropland land uses throughout our study period. We then summarized the data on a monthly time scale. 

Discharge (Q): We measured discharge at six catchments over the course of the study period (two forested, four cropland or mixed cropland/forest) In each study catchment, we installed permanent gauge stations, instrumented with Onset Hobo U20 level loggers, which recorded hourly stream level and water temperature throughout the study period. To estimate stream discharge, we established stream rating curves, relating co-located field measurements of stream discharge to logged level data.

Soil Moisture (dS/dt): Soil moisture was calculated using the Time Domain Reflectometry method (TDR). Over the course of the study period, six soil pits (three in croplands, three in forest) (Figure 1) were used for varying lengths of time (see Table 1 for timespan of each soil pit). Sensors were installed at 0m (surface), 0.3m, 0.5m, 1m and then every subsequent meter up to 8m for a total of eleven sensors per pit. Sensors at 0 and 0.3m were installed vertically, while all other sensors were inserted horizontally 0.5m into soil. After installation, pits were covered with plastic sheets to minimize evaporation. Volumetric water content was calculated using measured soil density and gravimetric water content collected from multiple samples in each soil pit prior to permanent installation. For more details on these calculations, see Silveiro et al. (2024). Soil moisture anomalies were calculated using the deviation from the annual mean for each soil pit for each water year.

Water balance calculations: We used a monthly time step (dt) to calculate the water balances (Eq 1.) for cropland and forest areas during normal periods, as well as the drought year. We found the calendar monthly average of dS and Q over the study period at each site and combined all cropland and forest sites to extract an average dS and Q for each land cover. We calculated Goutflow using Eq. 1 for each calendar month. Bootstrap analyses (iterations=1000) to quantify normal year distribution of P, ET, dS, Q and Goutflow were calculated using the means and standard deviations of the normal water balance over annual, wet season, and dry season time periods. All calculations were done in Python.



Precipitation (https://data.chc.ucsb.edu/products/CHIRPS-2.0/) and evapotranspiration (https://www.earthdata.nasa.gov/data/catalog/lpcloud-mod16a2-006) datasets are publicly available from their original sources. Discharge and soil moisture data utilized in this manuscript are available on CUAHSI Hydroshare (https://www.hydroshare.org/resource/64302ec32fd24341a61f3a0825ee6422/).

