# California Housing

## Source

This dataset is a modified version of the California Housing dataset available from Luís Torgo's page (University of Porto). Luís Torgo obtained it from the StatLib repository (which is closed now). The dataset may also be downloaded from StatLib mirrors.

This dataset appeared in a 1997 paper titled Sparse Spatial Autoregressions by Pace, R. Kelley and Ronald Barry, published in the Statistics and Probability Letters journal. They built it using the 1990 California census data. It contains one row per census block group. A block group is the smallest geographical unit for which the U.S. Census Bureau publishes sample data (a block group typically has a population of 600 to 3,000 people).

## Tweaks

The dataset in this directory is almost identical to the original, with two differences:

* 207 values were randomly removed from the total_bedrooms column, so we can discuss what to do with missing data.
An additional categorical attribute called ocean_proximity was added, indicating (very roughly) whether each block group.

* is near the ocean, near the Bay area, inland or on an island. This allows discussing what to do with categorical data.

## Data description

```python
>>> housing.info()
#   Column              Non-Null Count  Dtype  
---  ------              --------------  -----  
 0   longitude           20640 non-null  float64
 1   latitude            20640 non-null  float64
 2   housing_median_age  20640 non-null  float64
 3   total_rooms         20640 non-null  float64
 4   total_bedrooms      20433 non-null  float64
 5   population          20640 non-null  float64
 6   households          20640 non-null  float64
 7   median_income       20640 non-null  float64
 8   median_house_value  20640 non-null  float64
 9   ocean_proximity     20640 non-null  object 
dtypes: float64(9), object(1)

*************************************************************

>>> housing["ocean_proximity"].value_counts()

<1H OCEAN     9136
INLAND        6551
NEAR OCEAN    2658
NEAR BAY      2290
ISLAND           5
Name: ocean_proximity, dtype: int64
```

## create virtual environment

I use vscode with `cmd` to create a virtual environment with the following command:

> Creating virtual environment

```bash
python -m venv .venv 
```

Which python mean the `python.exe` location in your PC.

> Activating virtual environment

```bash
.venv/Scripts/activate 
```

> Installing requirements

```bash
pip install -r requirements.txt 
```
