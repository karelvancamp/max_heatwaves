# Description

Fig. 2. Projected change in the return period of the western North America heat extreme.
The chance of exceeding the current record in any given summer day of a year in each decade. The current record used is 40.1°C, an event with the same magnitude as the June 2021 observed event for the model climatology, for the western North America region of 45°N to 52°N, 119°W to 123°W. Each decade is centered on the value on the x axis, (e.g., 2015–2024). Simulations are from the CanESM5, using three different future scenarios (as labeled) and 50 ensemble members for each scenario. Values are the chance of an event on any given day (JJA) per year. The vertical lines represent the uncertainty, calculated as the range from individual ensemble members.

# Sources

https://gmd.copernicus.org/articles/12/4823/2019/gmd-12-4823-2019.html
The Canadian Earth System Model version 5 (CanESM5.0.3)

    mod_rcp85 = iris.load_cube('/user/home/hh21501/LargeEnsembles/USHeatwave/tmp/WWA_CanESM.nc') # JJA, 2015-2100
    mod_rcp45 = iris.load_cube('/user/home/hh21501/LargeEnsembles/USHeatwave/tmp/WWA_ssp245_CanESM.nc') # JJA, 2015-2100
    mod_rcp16 = iris.load_cube('/user/home/hh21501/LargeEnsembles/USHeatwave/tmp/WWA_ssp126_CanESM.nc') # JJA, 2015-2100


https://ccsr.aori.u-tokyo.ac.jp/ccsrlist/Description_of_MIROC6_AGCM.pdf
The sixth version of MIROC or Model for Interdisciplinary Research on Climate

    mod1a = np.load('/user/home/hh21501/LargeEnsembles/USHeatwave/tmp/WWA_miroc_20002010.nc.npy')
    mod1b = np.load('/user/home/hh21501/LargeEnsembles/USHeatwave/tmp/WWA_miroc_19901999.nc.npy')
    mod1c = np.load('/user/home/hh21501/LargeEnsembles/USHeatwave/tmp/WWA_miroc_19811989.nc.npy')
    mod1 = np.concatenate((mod1a, mod1b, mod1c))-273.15
    mod2 = iris.load_cube('/user/home/hh21501/LargeEnsembles/USHeatwave/tmp/WWA_miroc_20152024.nc')

ERA5

    obs = iris.load_cube('era_19602020.nc') # wwa region era5 daily max temp jja




