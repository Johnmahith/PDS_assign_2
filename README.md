# Used Car Price Prediction Data Preprocessing

This repository contains preprocessing code for a used car dataset aimed at predicting the prices of used cars. The dataset includes detailed attributes like make, model, year of manufacture, mileage, and more. The preprocessing steps prepare the data for machine learning models.

## Dataset Overview

- **Attributes**: Make, Model, Location, Year, Mileage, Odometer, Fuel Type, Transmission, Owners, Engine CC, Horsepower, Seats, Price (current and new).
- **Objective**: Clean and transform the data to predict used car prices.

## Preprocessing Summary

### Missing Values

- **Method**: Imputation for continuous variables (Mileage, Engine CC, Horsepower, Seats) with their median values. 
- **Rationale**: Median imputation was chosen to handle outliers and maintain the distribution of the data.

### Unit Conversion

- **Attributes Processed**: Mileage, Engine CC, Horsepower, New Price.
- **Action**: Removed textual units and converted values to numerical format for consistency.

### Categorical Encoding

- **Attributes**: Fuel Type, Transmission.
- **Method**: One-hot encoding to convert categorical variables into numerical format.
- **Rationale**: Enables the use of these categorical variables in machine learning models.

### Feature Engineering

- **New Feature**: Car Age.
- **Calculation**: Current year (2024) minus the year of manufacture.
- **Purpose**: Provides additional insight into the vehicle's value depreciation over time.

### Data Transformation

- **Operations**: Select, filter, rename, mutate, arrange, summarize with group by.
- **Example Operations**:
  - Filtered cars older than 10 years.
  - Renamed 'Kilometers_Driven' to 'KMs_Driven'.
  - Added 'Price_Per_Year' as a new column.
  - Summarized average price and kilometers driven by location.

## Usage

- **Requirements**: Python, Pandas, NumPy.
- **Instructions**: Load your dataset and run the provided script to apply the preprocessing steps. Adjust the file path to your dataset location.

