# Week 3 — Two Averages, One Argument

## 1. My understanding of the task

In this assignment, I need to analyse the price data using averages and percentage changes. I will compare the mean and median and consider how a flagged value can affect the results.

## 2. Predictions before calculating

- I think the mean and median will be different for some items because the prices are not always the same.
- I expect the flagged value to increase the mean because it is much higher than the other prices.
- I think the median will change less when the flagged value is excluded.
- I expect the first-to-last percentage change to show whether prices increased or decreased over the period.

## 3. My calculation plan

For each item, I will calculate:

- Mean price
- Median price
- First-to-last percentage change separately for each city

The formula used for percentage change is:

Percentage change = ((Last price − First price) / First price) × 100

### Results

| Item | Mean | Median |
|---|---:|---:|
| Staple A | 160.89 | 112.50 |
| Oil B | 316.18 | 324.00 |
| Pulse C | 205.91 | 206.00 |
| Sweetener D | 576.81 | 167.75 |

### First-to-last percentage change

| Item | City 1 | City 2 |
|---|---:|---:|
| Staple A | 13.37% | 12.62% |
| Oil B | 15.44% | 15.13% |
| Pulse C | 3.75% | 2.40% |
| Sweetener D | 19.80% | 19.03% |

For Pulse C in City 2, the first available price was used because the price on 1 January was missing. The first available observation was on 8 January.

## 4. Flagged-value comparison

Item selected: Sweetener D

| Measure | Flag included | Flag excluded |
|---|---:|---:|
| Mean | 576.81 | 167.15 |
| Median | 167.75 | 167.50 |

The flagged observation is 9,999 for Sweetener D in City 1.

My observation about the difference:

The mean increases significantly when the flagged value is included, while the median only changes slightly. This shows that an unusually high value can have a much bigger effect on the mean than on the median.

## 5. Initial interpretation

- **Observation:** The mean and median are quite close for Oil B and Pulse C.
- **Observation:** Sweetener D has a much higher mean than median when the flagged value is included.
- **Possible explanation:** The high flagged value is affecting the mean because the mean takes every observation into account.
- **Observation:** Sweetener D has a positive first-to-last percentage change in both cities.
- **Possible explanation:** Prices may have generally increased over the period, but the percentage changes alone do not explain why.
- **Causal claim:** I cannot establish a cause for the price increases from these calculations alone.

## 6. Questions I have

1. Should a flagged value always be removed, or should it be kept and explained?
2. Is the median a better measure when the dataset contains unusually high values?
3. Can percentage changes alone be used to explain why prices increased?