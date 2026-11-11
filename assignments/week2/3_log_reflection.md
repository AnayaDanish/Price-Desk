# Assignment 2 – AI Check and Reflection

## Court Verdict

1. `clean = raw.copy()`  
   **Verdict: Keep** – Creates a separate copy so the original dataset is not changed.

2. `clean["price"] = clean["price"].str.replace(",", "", regex=False)`  
   **Verdict: Keep** – Removes commas from the price values, such as changing 1,250 into 1250.

3. `clean["price"] = pd.to_numeric(clean["price"], errors="coerce")`  
   **Verdict: Keep** – Converts the price column from text into numerical values (float64). I checked that the missing price remained 1 after conversion.

4. `clean["date"] = pd.to_datetime(clean["date"], errors="coerce")`  
   **Verdict: Keep** – Changes the date column into datetime format so that dates can be sorted properly.

5. `clean = clean.drop_duplicates()`  
   **Verdict: Keep** – Removes one exact duplicate row after I checked that both observations contained the same information.

6. `clean["price_flag"] = clean["price"] == 9999`  
   **Verdict: Keep** – Flags the unusual price of 9999 without deleting or changing the original value.

7. `clean = clean.sort_values("date")`  
   **Verdict: Keep** – Arranges the dataset in chronological order without changing the actual observations.

8. `clean.to_csv("teaching_prices_cleaned.csv", index=False)`  
   **Verdict: Keep** – Saves the cleaned dataset as a separate CSV file.

## CHECK

**Was any valid observation removed?**  
No. Only one exact duplicate observation was removed.

**Were any labels or numbers changed without my knowing?**  
No. The comma in the price value was removed to make it numerical. The unusual price of 9999 was preserved.

**Did the missing values increase after cleaning?**  
No. There was still only 1 missing price after converting the column into numbers.

**Does the final dataset have the expected number of rows and columns?**  
Yes. It has 96 rows and 7 columns. One duplicate row was removed, and one new column (`price_flag`) was added.

**Were the unusual values handled properly?**  
Yes. The price of 9999 was flagged for further investigation instead of being deleted.

## REFLECTION

Most of the cleaning suggestions from AI were useful and matched what I had identified during my initial inspection. However, I still had to check the results after running each code.

One important thing I learned was that converting a column into numbers can sometimes create additional missing values if the formatting is not handled first. This is why I removed the comma from the price value before converting it.

I also decided not to delete the unusual price of 9999 or fill in the missing price because I did not have enough evidence to make those changes.

Overall, AI helped me understand and organise the cleaning process, but checking the outputs was important to make sure the data was not changed incorrectly.

## LOG ROWS

**Date and task:** 12 November 2026 – Cleaning the teaching prices dataset.

**Prompt or excerpt:** Described my dataset (97 rows and 6 columns) and the problems I found, including a missing price, duplicate row, inconsistent price formatting, unusual price and unsorted dates. Asked for cleaning code that would work on a copy of the original dataset.

**How I verified it: Checked the missing values, data types, duplicate count, unusual price and final dataset shape before and after cleaning.

Accepted / modified / rejected: Accepted most of the suggested cleaning steps. Modified the approach to price conversion by removing commas before converting the values into numbers.

Reason: The cleaning steps matched the problems I had identified and the results were consistent with my checks.

What could have gone wrong if I had not checked: The unusual price could have been deleted without evidence, the missing price could have been filled incorrectly, or a valid observation could have been removed. Also, an incorrectly formatted price could have been converted into a missing value.
