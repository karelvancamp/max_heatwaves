# Description

Table 1. Top heat extremes that are consistent between datasets.

Lists all events over 4 SDs (relative to the climate of the previous decade) from the mean in either ERA5 or JRA55, and consistent between the two datasets (see Materials and Methods). Because of the time periods covered by the reanalyses, only events from 1968 onward can be considered. The magnitude in terms of SD and absolute temperature, and the SD for both ERA-5 and JRA55 are included. Comments on the time scale and spatial extent of the events are included in the notes column.

# Code

- reg_mean_calc_ERA5.m
- miroc_run_plume_v2.py
- ??? 

Assumed pseudo logic: 

    for all frames in generated TS ERA5 or MIROC 
    where region not in inconsistent regions 
        mask_regs from Alan: not clear how calculated.
    where sd = number of SDs from the mean based on 10-year rolling
    where metric sd >= 4
    show results from merged frames ERA5 and MIROC
    sort by max(sdERA5, sdMIROC) desc


## consistent between the two datasets



    mask_regs = [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,0,1,1,1,1,1,1,1,1,1,1,1,1,1,1,0,1,1,0,0,1,1,0,1,1,1,1,0,1,1,1,1,1,0,0,1,0,0,1,0,0,1,0,0,0,0,0,0,0,1,0,0,0,0,0,0,1,0,1,0,1,1,0,1,1,1,0,0,0,0,0,0,0,0,0,0,0,0,0,1,1,1,0,1,1,1,1,1,1,1,1,1,1,1,1,0,1,1,0,1,1,1,0,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,0,1,1,0,1,1,1,1,1,1,0,0,1,1,1,1,1,1,0,0,1,0,0,0,1,0,1,1,1,1,1,0,1,0,1,0,0,0,1,1,1,0,1,0,0,1,1,0,0,0,1,0,1,0,0,1,1,1,1,1,1,1,1,1,1,1,0,1,1,1,1,1,1,1,1,0,0,0,1,1,0,1,1,0,1,0,1,1,0,0,1,1,0,1,1,1,0]


