# Task 3: Data Cleaning Project
**Objective:** Take a messy dataset (`trx-10k.csv.xlsx`) and clean it up step-by-step so it can be used for data analysis.

## 1. What the Data Looked Like First
When I first loaded the dataset, I checked its quality to see what needed fixing:
* **Total Rows:** 10,000
* **Missing Data:** I found 427 missing values.
* **Data Types:** Dates were just text, IDs had decimals (like `98.0`), and the amounts had weird negative numbers (like `-999999.0`).
* **Text Problems:** There were a lot of typos like `Tehr@N`, `Vsa`, and `succeed`.

## 2. Removing Duplicates
First, I checked for duplicate rows.
* **Result:** There were 0 duplicate rows, so we still have 10,000 rows.

## 3. Fixing Text Columns
There were a lot of spelling mistakes in the text columns.
* **Status:** I changed things like `succeed`, `failed`, and `Success` into just `"Success"` or `"Fail"`.
* **Card Type:** I fixed typos like `Vsa` to `"Visa"`, and `mastcard` to `"Mastercard"`.
* **City:** I changed spelling variations like `thr`, `Thran`, and `Tehr@N` to `"Tehran"`. I also changed `Nan` to `"Unknown"`.

## 4. Fixing Data Types
I had to convert columns into the right format so we can do math on them later.
* **time:** Changed to `datetime`.
* **id:** Changed from numbers (like `98.0`) to strings (`"98"`).
* **amount:** Changed to float. I also turned those weird `-999999.0` placeholders into missing values (`NaN`) so I could easily fix them in the next step.

## 5. Handling Missing Data
There were 427 missing values to deal with.
* For the **amount** (numbers), I filled the missing spots with the **Median** because the median is better to use when there are extreme outliers.
* For the text columns, I filled the missing spots with the **Mode** (the most common value) or `"Unknown"`.

## 6. Fixing Outliers
There were some really extreme numbers in the dataset.
* I used the **IQR (Interquartile Range) Method** to find them.
* Instead of deleting those rows, I **capped** them to the maximum and minimum boundaries so we don't lose the rest of the row's data.

## 7. Before vs. After Summary

| Metric | Before Cleaning | After Cleaning |
| :--- | :--- | :--- |
| **Total Rows** | 10,000 | 10,000 |
| **Missing Values** | 427 | 0 (Filled with median/mode) |
| **Data Types** | Messy and wrong | All correct |
| **Text Columns** | Full of typos | 100% clean and consistent |

## 8. Final Output
I saved the final clean data as **`cleaned_dataset.csv`**.
