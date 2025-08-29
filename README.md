# Uber Ride Data Analysis (2016)

## Project Overview

This project performs an in-depth exploratory data analysis (EDA) on the Uber rides dataset from 2016. The primary objective is to uncover travel patterns, identify key trends, and derive actionable insights from the ride data. By cleaning, processing, and visualizing the dataset, we can answer questions related to trip frequency, purpose, timing, and popular routes. This analysis provides a comprehensive look at how Uber was utilized for personal and business travel throughout the year.

---

## Dataset

The analysis is based on the **UberDataset.csv** file, which contains data on over 1,150 Uber rides. The key columns in the dataset include:

* **START_DATE**: The date and time when the ride started.
* **END_DATE**: The date and time when the ride ended.
* **CATEGORY**: The category of the trip (Business or Personal).
* **START**: The starting location of the ride.
* **STOP**: The destination of the ride.
* **MILES**: The total miles of the trip.
* **PURPOSE**: The purpose of the trip (e.g., Meeting, Meal/Entertain).

---

## Analysis and Key Steps

The project follows a structured approach to data analysis:

1.  **Data Loading and Inspection**: The dataset was loaded into a pandas DataFrame, and initial inspections (`head()`, `info()`, `shape`) were performed to understand its structure, data types, and size.

2.  **Data Cleaning and Preprocessing**:
    * Checked for and handled missing values. Null values in the `PURPOSE` column were filled using the forward-fill method (`ffill`).
    * Converted the `START_DATE` and `END_DATE` columns from object (string) types to a proper `datetime` format to enable time-based analysis.

3.  **Feature Engineering**:
    * New columns were created by extracting valuable information from the `START_DATE` column, including:
        * `month`
        * `day of the week`
        * `hour`
    * This step enriched the dataset, making it possible to analyze trends based on specific time components.

4.  **Exploratory Data Analysis (EDA) and Visualization**: A series of visualizations were created using **Matplotlib** and **Seaborn** to answer key business questions and reveal patterns in the data.

---

## Visualizations and Key Insights

The analysis yielded several important insights into Uber usage patterns:

### 1. Trip Category Breakdown

A count plot of the **`CATEGORY`** column clearly shows that **Business trips are far more frequent** than Personal trips in this dataset, indicating a strong use of Uber for professional purposes.

### 2. Most Common Trip Purposes

The analysis of the **`PURPOSE`** column reveals that **"Meeting"** is the most common reason for an Uber ride, followed closely by **"Errand/Supplies"**. This reinforces the business-oriented nature of the trips.

### 3. Monthly and Daily Ride Patterns

* **Monthly Trends**: By counting trips per month, it was found that **December was the busiest month** for Uber rides.
* **Daily Trends**: The analysis of the `day of the week` showed that **Friday is the busiest day**, suggesting a peak in travel towards the end of the workweek.

### 4. Peak Hours for Uber Rides

A line plot visualizing the number of trips by the hour reveals that Uber rides peak in the **late afternoon and evening**, likely corresponding with the end of the workday and evening appointments.

### 5. Most Frequent Routes

The analysis of **`START`** and **`STOP`** locations identified the most popular travel routes. **Cary to Morrisville** and **Morrisville to Cary** were found to be the most frequent trips, suggesting a common commute or business corridor.

### 6. Correlation of Features

A heatmap was generated to visualize the correlation between numerical features like `MILES`, `month`, and `hour`. This helps in understanding the relationships between different variables in the dataset.

---

## Tools and Libraries Used

* **Python**: The core programming language for the analysis.
* **Pandas**: For data manipulation, cleaning, and processing.
* **NumPy**: For numerical operations.
* **Matplotlib**: For creating foundational plots and visualizations.
* **Seaborn**: For creating more advanced and aesthetically pleasing statistical plots.

---

## Conclusion

This project successfully transformed raw Uber ride data into meaningful insights. The analysis highlights that Uber in 2016, for this user, was primarily a tool for business, with clear patterns emerging around work-related purposes, peak travel times, and common routes. These findings demonstrate the power of data analysis in understanding user behavior and service utilization.
