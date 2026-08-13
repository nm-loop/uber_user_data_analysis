# Uber User Data Analysis

An Exploratory Data Analysis (EDA) project based on Uber user/trip data.
The project uses Python and popular data analysis and visualization
libraries to understand trip patterns, mileage distribution, travel
timing, monthly trends, and unusual observations in the dataset.

## Project Overview

The dataset contains Uber trip records with information such as:

-   Start and end date/time
-   Trip category
-   Starting location
-   Destination
-   Distance traveled in miles
-   Trip purpose

The analysis also creates additional features such as date, time,
day/night category, month, and day of the week.

## Dataset

The original dataset contains **1,156 rows and 7 columns**.

### Original Columns

  Column         Description
  -------------- --------------------------
  `START_DATE`   Trip start date and time
  `END_DATE`     Trip end date and time
  `CATEGORY`     Trip category
  `START`        Trip starting location
  `STOP`         Trip destination
  `MILES`        Distance traveled
  `PURPOSE`      Purpose of the trip

### Additional Features

During preprocessing and feature engineering, the project creates:

-   `date` -- extracted date from `START_DATE`
-   `time` -- extracted hour from `START_DATE`
-   `day-night` -- time-based category such as Morning, Afternoon,
    Evening, or Night
-   `MONTH` -- month extracted from the trip date
-   `DAY` -- day of the week

## Technologies Used

-   Python
-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   Jupyter Notebook

## Project Workflow

The analysis follows these main steps:

1.  Import required Python libraries.
2.  Load the Uber dataset using Pandas.
3.  Explore the dataset using functions such as `head()` and basic
    inspection.
4.  Convert date columns into datetime format.
5.  Extract useful date and time features.
6.  Categorize trips according to time of day.
7.  Analyze monthly and daily trip patterns.
8.  Analyze the `MILES` variable.
9.  Detect potential outliers using boxplots.
10. Study mileage distribution using histograms and KDE.
11. Visualize important patterns using Matplotlib and Seaborn.

## Exploratory Data Analysis

### Mileage Analysis

The `MILES` column is analyzed to understand the typical distance of
Uber trips.

A boxplot is used to identify unusually high mileage observations. The
analysis shows that most trips are relatively short, while some trips
have considerably higher mileage.

A filtered analysis of trips below 100 miles and below 40 miles is also
used to examine the main distribution more clearly.

### Distribution Analysis

A histogram with KDE is used to understand the distribution of trip
distances.

The distribution of trips below 40 miles is concentrated toward lower
mileage values and has a longer tail toward higher values, indicating a
**right-skewed distribution**.

### Time and Day/Night Analysis

The trip start time is extracted from `START_DATE` and grouped into
categories such as:

-   Morning
-   Afternoon
-   Evening
-   Night

This helps analyze when trips are commonly made.

### Monthly Analysis

The month is extracted from the trip start date and used to analyze trip
patterns across the year.

## Key Observations

-   The dataset contains 1,156 trip records.
-   Most recorded trips are relatively short-distance.
-   Several high-mileage observations appear as potential outliers.
-   The mileage distribution is positively/right-skewed.
-   Date and time features can be used to study travel behavior across
    months, days, and different times of the day.

## Repository Structure

``` text
Uber-User-Data-Analysis/
│
├── UberDataset.xlsx
├── project.ipynb
├── README.md
```

## How to Run

1.  Clone or download this repository.
2.  Make sure Python is installed.
3.  Install the required libraries:

``` bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

4.  Open the Jupyter Notebook:

``` bash
jupyter notebook
```

5.  Run the notebook cells sequentially.

## Conclusion

This project demonstrates a practical Exploratory Data Analysis workflow
using Uber trip data. It covers data preprocessing, feature engineering,
statistical exploration, outlier detection, and visualization to
understand trip behavior and mileage patterns.

## Author

**Niraj Kumar Maurya**
