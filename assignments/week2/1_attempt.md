# Assignment 2 – Initial Attempt

## THINK Stage

I started by loading the dataset and looking through the rows to understand what kind of data it contains. The dataset has 97 rows and 6 columns: date, item, city, price, unit and data_label.

I used a few basic pandas commands to check the dataset and found some issues.

### 1. Missing values

I used `raw.isna().sum()` to check for missing values.

I found that there is 1 missing value in the price column. It is for Pulse C in City 2 on 1 January 2026.

I think this should be investigated first because we don't know what the actual price was.

### 2. Duplicate rows

I used `raw.duplicated().sum()` and found 1 duplicate row.

The repeated observation is for Staple A in City 1 on 8 January 2026, with a price of 99.5.

This seems to be an accidental duplicate, but I would check it before removing it.

### 3. Price formatting

While checking the unique values in the price column, I noticed that most prices are written as numbers in string format. However, one value is written as `1,250` instead of the usual format.

This could cause problems when doing calculations, so it may need to be converted into a proper numeric value.

### 4. Unusual price

I also noticed a price of `9999` for Sweetener D in City 1 on 22 January 2026.

This seems unusually high compared to the other prices. It could be a mistake, but I cannot be sure without checking it further, so I would flag it rather than delete it.

### 5. Data types

When I used `raw.info()`, I noticed that the columns were stored as strings.

The date and price columns should probably have more suitable data types so that I can use them properly for sorting and calculations.

### 6. Date order

When I checked the last few rows, I noticed that the dates were not in chronological order.

This might just mean that the dataset is not sorted properly, so I would check the dates and sort them if needed.

## Initial conclusion

Overall, I found a few problems in the dataset, mainly a missing price, a duplicate row, inconsistent price formatting and an unusual price value. I have not changed the original dataset yet because I want to understand each issue before deciding what to do with it.
