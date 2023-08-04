## Fig1

For generic rework:

Input parameters
- choose timeframe
- BBox or contour region of intrest

Additions?
- relative humidity
  
Can be fetched from https://cds.climate.copernicus.eu/apps/user-apps/app-c3s-daily-era5-statistics?

> pera5: "/bp1store/geog-tropical/data/ERA-5/"

## Statistics of the heat wave in the western North America

(A) Time series plot of observed daily maximum temperatures for the last week of June and first week of July in the region 45°N to 52°N, 119°W to 123°W, 
from 1950 to present. (B) Distribution of the 1950–2020 temperatures shown in (A). 

### tasmax, this is from 1950!

https://cds.climate.copernicus.eu/apps/user-apps/app-c3s-daily-era5-statistics?dataset=reanalysis-era5-single-levels&product_type=reanalysis&variable_e5sl=2m_temperature&pressure_level_e5sl=-&statistic=daily_maximum&year_e5sl=2023&month=06&frequency=1-hourly&time_zone=UTC%2B00:00&grid_e5=0.25/0.25&area.lat:record:list:float=45&area.lat:record:list:float=52&area.lon:record:list:float=119&area.lon:record:list:float=123              

- dataset=reanalysis-era5-single-levels
- variable_e5sl=2m_temperature
- statistic=daily_maximum

- year_e5sl=2023&month=06
- frequency=1-hourl
- area.lat:record:list:float=45&area.lat:record:list:float=52&area.lon:record:list:float=119&area.lon:record:list:float=123              
- grid_e5=0.25/0.25 => only observe small area

> fjun = glob.glob(pera5+"day/tasmax/*_*06.nc")
> fjul = glob.glob(pera5+"day/tasmax/*_*07.nc")

## geopotential height at 500 hPa

(C) Scatter plot of geopotential height at 500 hPa (Z500) over the 2-week period 24 June to 7 July versus precipitation 
minus evaporation (P-E) over June, with both axes showing values averaged over the area of interest. 
Each dot represents 1 year between 1950 and 2021. 

### z500, from 1950
        
https://cds.climate.copernicus.eu/apps/user-apps/app-c3s-daily-era5-statistics?dataset=reanalysis-era5-pressure-levels&product_type=reanalysis&variable_e5pl=geopotential&pressure_level_e5pl=500&statistic=daily_mean&year_e5pl=2023&month=06&frequency=1-hourly&time_zone=UTC%2B00:00&grid_e5=0.25/0.25&area.lat:record:list:float=45&area.lat:record:list:float=52&area.lon:record:list:float=119&area.lon:record:list:float=123

- dataset=reanalysis-era5-pressure-levels
- variable_e5pl=geopotential
- pressure_level_e5pl=500
- statistic=daily_mean

> fjun_z = glob.glob(pera5+"day/z/z500/*_*06.nc")
> fjul_z = glob.glob(pera5+"day/z/z500/*_*07.nc")

### precip, from 1950

https://cds.climate.copernicus.eu/apps/user-apps/app-c3s-daily-era5-statistics?dataset=reanalysis-era5-single-levels&product_type=reanalysis&variable_e5sl=total_precipitation&pressure_level_e5sl=-&statistic=daily_maximum&year_e5sl=2023&month=06&frequency=1-hourly&time_zone=UTC%2B00:00&grid_e5=0.25/0.25&area.lat:record:list:float=45&area.lat:record:list:float=52&area.lon:record:list:float=119&area.lon:record:list:float=123

- dataset=reanalysis-era5-single-levels
- variable_e5pl=total_precipitation
- statistic=daily_mean

> fps_1 = glob.glob(pera5+"day/total_precipitation/*_*06.nc")
> fps_2 = glob.glob(pera5+"day/total_precipitation/*_*07.nc")

### evaporation, from 1950

https://cds.climate.copernicus.eu/apps/user-apps/app-c3s-daily-era5-statistics?dataset=reanalysis-era5-single-levels&product_type=reanalysis&variable_e5sl=evaporation&pressure_level_e5sl=-&statistic=daily_maximum&year_e5sl=2023&month=06&frequency=1-hourly&time_zone=UTC%2B00:00&grid_e5=0.25/0.25&area.lat:record:list:float=45&area.lat:record:list:float=52&area.lon:record:list:float=119&area.lon:record:list:float=123

- dataset=reanalysis-era5-single-levels
- product_type=reanalysis
- variable_e5pl=evaporation
- statistic=daily_mean
        
                # fep_1 = glob.glob(pera5+"day/evaporation/*_*06.nc")
                # #fep_2 = glob.glob(pera5+"day/evaporation/*_*07.nc")

## (D) Northward component of wind at 500 hPa in the Northern Hemisphere, averaged over the same 2-week period in 2021;

### v500, june july 2021

https://cds.climate.copernicus.eu/apps/user-apps/app-c3s-daily-era5-statistics?dataset=reanalysis-era5-pressure-levels&product_type=reanalysis&variable_e5pl=vertical_velocity&pressure_level_e5pl=500&statistic=daily_mean&year_e5pl=2023&month=06&frequency=1-hourly&time_zone=UTC%2B00:00&grid_e5=0.25/0.25&area.lat:record:list=&area.lat:record:list=&area.lon:record:list=&area.lon:record:list=

- dataset=reanalysis-era5-pressure-levels
- variable_e5pl=vertical_velocity
- pressure_level_e5pl=500
- statistic=daily_mean

> fj21_v = "/user/home/yl17544/ERA5_extras/ERA5_v500_hour_20210607.nc"    

Gray box over western North America indicates the region assessed: 45°N to 52°N, 119°W to 123°W.