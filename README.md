# Pyber_Analysis


# Overview
- A 2019 financial summary was requested as well as weekly fares generated in each city type in first quarter plotted onto a line graph. We were given the data in two csv files that we first merged together in Pandas. The data was broken down from the merged .csv files into city types, and was processed using the `groupby()` function to find the total number of fares, drivers, and rides for each type. We calculated the average fares per ride and fares per driver and created the financial summary.
- For the graph, we made a new dataframe that contained the date, fares, and city type. Using the `groupby` function, we grouped the date and city type and calculated the total fares for each type for every timestamp. We reset the index to convert the date series from a float to timestamp and applied `.resample('W').sum()` to group the dates into weekly increments and total up the fares for each week. Finally, the multiple line graph was shaped using `fig,axs = plt.subplots(figsize = (20,6))` and the data was plotted using `fares_by_week.plot(ax=axs)`.

## Results
- In the financial summary below: 

![pybersummarydf](https://github.com/taherrin92/Pyber_Analysis/blob/main/analysis/Pyber_summarydf.png)


-The total fares in urban areas are the highest by a large margin with $39,854.38, but the average fare of $16.57 per driver is the lowest. The opposite is true for rural areas, where the total fares of $4,327.93 are the lowest but sees the highest average fare per driver at $55.49. Urban areas are the only city type that employ more drivers than total rides. 
The average fare per ride in urban towns is only 30% lower than in rural areas, but the average fare per driver in urban areas is 70% less than rural towns. 

