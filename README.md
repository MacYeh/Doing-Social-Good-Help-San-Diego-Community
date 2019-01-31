# Help-San-Diego-Community-

**Doing Social Good for Local San Diego Community**

`Who Gets Stopped by San Diego Police`

What are the demographics of people who get stopped for traffic violations, why are they stopped, and how do their demographics compare to the areas where they are stopped?


## Getting Started

Python and iPython Notebook are used 

### Prerequisites

The following Python Libraries are used in this investigation

```

1. os
2. glob
3. pandas
4. geopandas
5. matplotlib
6. seaborn
7. numpy
8. folium

```

## End to End Flow

```

1. Dataset Investigation and Clean
2. Data Analysis on the relation between age/sex and stop-cause
3. Relation Analysis between Race and Stop-Cause
4. Relation Analysis between Race and Regions on the certain Stop-Cause
    1. Moving Violation
    2. Equipment Violation

```

### Data Investigation and Clean

There are two different categories of data involved in this project:
1. Vehicle Stops Data from 2014 to 2017 and Race Code Translation => [Data Source](https://data.sandiego.gov/datasets/police-vehicle-stops/)
2. Demographic Data based on Police Beat Region => [Data Source](https://data.sandiegodata.org/dataset/sandiego-gov-police_regions)

We highly utilize [Pandas](https://pandas.pydata.org/) to wrangle the data like SQL way. It includes the following `Pandas` functions: 
1. `Join`
2. `Apply`
3. `Groupby`
4. `Rank`

In addition to `Pandas`, we also have to incoperate `GeoPandas` [GeoPandas](http://geopandas.org/) to retrieve the geojson data and save as DataFrame format

Before the further data analysis, we would like to `clean` and `reasonably manipulate` the data which would avoid the missed interpretation later 

### Data Analysis on the relation between age/sex and stop-cause

The flow includes:
1. `Data Wrangle`
2. `Visualization Results`
3. `Observation and Conclusion`

#### Data Wrangle

Remember ***`Filter`*** way in Pandas to clean sex X

#### Visulization and Results

Utilize 
1. **`Seaborn Distribution``**
2. **`Seaborn FacetGrid`** to have multiple plotts with different stop-causes
3. **`Seaborn HeatMap`** to visualize the relation between age and stop cause

#### Observation and Conclusion

With the distributions and the heatmaps, two pull-over reaons from San Diego PD are 

1. **Moving Violation**
2. **Equipment Violation**

These reason counts make sense with the understanding and encountering of our daily life.

We also observe the pull-over rate with the age distribution and sex distribution.

The people with the **age 20 to 29** are inclined to be pulled over with the spotting moving violation. With the age increases, the pull-over rate is reduced. It also might explain the insurance company will have the high premium at this range of the age. The ***male*** drivers are also intended to be pulled compared to ***female*** drivers. 

### Relation Analysis between Race and Stop-Cause

The flow includes:
1. `Data Wrangle`
2. `Visualization Results`
3. `Observation and Conclusion`

#### Data Wrangle

Remember ***`GroupBy and Pivot`*** ways in Pandas to aggregate the counts

#### Visulization and Results

Utilize 
1. **`Seaborn HeatMap`** to visualize the relation between Race and stop cause

Note: we were using the concept of [Per Capita Rate](https://www.robertniles.com/stats/percap.shtml)

#### Observation and Conclusion

We plot the per-capita rate on the total population at San Diego of each race group and the stop causes. It turns out the first two race groups violating the moving and equipment rules in terms of per-capita rate are **the American Indian** and **the Black**. The American Indian per-capita rate is even larger than 0.5 from the heatmap, the stopping cause data does not reveal the details if the same driver is recorded to different violation cases, however. This is the point we have to consider before interpreting the data based on per-capita

### Relation Analysis between Race and Regions on the major Stop-Cause

#### Moving Violation

![Moving](https://github.com/MacYeh/Help-San-Diego-Community-/blob/master/police_pull_over/figure/service_area_race_moving_per_capita.png)

We have the per-capita rate between the top 8 most beat areas on moving violation and the different racial groups. The per-capita rate is calculated with each racial population of beat areas. The results show at the certain beat areas, like **120** (which is mainly the **Mission Bay/La Jolla regions**), the Black race has the highest rate, the American Indian race has the highest ratethe at beat area, like **240** (which is mainly **Mira Mesa region**). The heatmap also shows per-capita rate is high among all race-groups at Beat **520** (which is **Downtown Region**). The American Indian per-capita rate is even larger than 1 at some regions, the stopping cause data does not reveal the details if the same driver is recorded to different violation cases, however. This is the point we have to consider before interpreting the data based on per-capita.

#### Equipment Violation

![Equipment](https://github.com/MacYeh/Help-San-Diego-Community-/blob/master/police_pull_over/figure/service_area_race_equipment_per_capita.png)

We have the per-capita rate between the top 8 most beat areas on equipment violation and the different racial groups. The per-capita rate is calculated with each racial population of beat areas. The results show at the certain beat areas, like **240** and **930** (which is mainly the **Mira Mesa and Del Mar/Carmal Valley Regions**), the American Indian race has the highest rate which is even larger than 1. Note that the stopping cause data does not reveal the details if the same driver is recorded to different violation cases, however. This is the point we have to consider before interpreting the data based on per-capita. Beat Area **930** (**Del-Mar and Carmal Valley Regions**) lead to the higher per-capita rate for some of the groups.


