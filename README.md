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

In addition to `Pandas`, we also have to incoperate [GeoPandas](http://geopandas.org/) to retrieve the geojson data and save as DataFrame format

### Data Analysis on the relation between age/sex and stop-cause

#### Data Wrangle

#### Visulization and Results

### Relation Analysis between Race and Stop-Cause

#### Data Wrangle

#### Visulization and Results

### Relation Analysis between Race and Regions on the certain Stop-Cause

#### Moving Violation

#### Equipment Violation

