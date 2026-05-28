# Lab – Interpret Visualizations with Respect to Outliers

## Objectives
In this lab, charts and functions will be used to detect data outliers.
* **Part 1:** Examine a Dataset for Outliers

## Background / Scenario
An outlier is a value or data point that varies significantly from others in the same dataset. An outlier can result from variability in the measurements, experimental errors, or human error in entering the data.

To make sure that any data analysis is correct, outliers need to be identified and then it needs to be determined how best to treat them.

## Required Resources
* Mobile device or PC/laptop with a browser
* Microsoft 365 Excel online
* Internet access

> **Note:** The precise steps to format and manipulate data in Excel can vary between platforms and versions. The instructions in this lab are based on the free version of Excel available from *Office.com* and may have to be modified to match the platform or version used to achieve the results shown in this lab.

---

## Instructions

### Part 1: Examine a Dataset for Outliers

#### Step 1: Open the data set
1. Download the file `Bike Sales_Outlier_Lab.xlsx`.
2. Upload the file to your OneDrive and open it in **MS 365 Excel online**.

#### Step 2: Use a Pivot Table to Select Data for Analysis
1. Click any cell in the **Bike Sales** worksheet.
2. Insert a pivot table by clicking **Insert > PivotTable**. 
3. Check that **New Worksheet** is selected in the *Create PivotTable* dialog box and click **OK**. 
   * *This adds a new worksheet for the pivot table.*
4. In the *PivotTable Fields* Dialog box, check the **Date** and **Order_Quantity** fields. 
   * *The pivot table is created with two columns: `Date` and `Sum of Order_Quantity`.*

#### Step 3: Sorting Data to Find Outliers
One way to identify outliers is by just sorting the data. This method works well with small data sets where the data is easily scanned.

1. **Sort the Sum of Order_Quantity column from high to low:**
   * Select the data points in the **Sum of Order_Quantity** column. *(Do not select the Grand Total or the column header).*
   * Click **Sort & Filter > Sort Descending**. 
   * *This sorts the Order_Quantity data points from highest to lowest.*

> **Question 1:** Which December date had the largest sales quantity? What was the sales quantity?
> 
> **Answer:** *[Enter your answer here]*

> **Question 2:** Review the data in the Bike Sales worksheet for December 19th. Which entry contributes most to the Sum of Order_Quantity in the pivot table? In other words, which order number is most responsible for the outlier?
> 
> **Answer:** *[Enter your answer here]*

#### Step 4: Use a Scatter Chart to Find Outliers
A scatter chart can help to identify outliers, especially in larger datasets.

1. Return to the worksheet containing the pivot table (`Sheet1`).
2. Copy and paste the data from the pivot table into two blank columns (**D** and **E**). Copy the header row with the data, but **do not copy the Grand Total row**.
   * *Note: Excel will not allow the creation of a scatter plot directly from data inside a pivot table. This is why the data must be moved to independent columns.*
3. **Insert the scatter plot:**
   * Select all cells in the copied data and use **Sort & Filter** to sort it ascending.
   * Highlight only the **Sum of Order_Quantity** column in your copied data.
   * Click on **Insert > Scatter** and then select the top-left scatter plot icon from the dropdown list.
   * *Notice that the visual layout of the scatter chart makes the sales for December 19th easily stand out as an outlier compared to the rest of the points.*
4. Delete the scatter plot when finished viewing.

#### Step 5: Using the LARGE and SMALL Functions to Find Outliers
If you are dealing with a large volume of data, the `LARGE` and `SMALL` functions can quickly extract the highest and lowest values to spot anomalies.

*For this example, assume your copied Date column is column **D** and your Sum of Order_Quantity column is column **E**. If your columns are different, adjust your function references accordingly.*

1. In an empty cell, enter the function: `=LARGE($E$4:$E27,1)`
   * *This function scans the entries from cell E4 through E27 and returns the absolute highest value.*

> **Question 3:** What value was returned by the function?
> 
> **Answer:** *[Enter your answer here]*

2. To get the top 5 highest values at once, modify the function to: `=LARGE($E$4:$E27, ROW($1:5))`
   * *This returns the highest five values. To return a different count, simply change the "5" at the end of the function to your desired number.*

> **Question 4:** What function would return the lowest 6 values?
> 
> **Answer:** `=SMALL($E$4:$E27, ROW($1:6))`

---

## Dealing with Outliers

Once outliers are identified, a data analyst must decide how to handle them. Outliers may indicate data errors, or they may be valid points that warrant a business investigation. Two common handling methods include:

* **Delete them:** In a very large dataset, deleting a few outliers will likely not impact the overall trends. However, always create a copy of the original data first so you can research what caused the outlier. In this lab's example, row 72 in the Bike Sales dataset could be safely deleted if proven to be an error.
* **Normalize them (Adjust their value):** The value of the outlier is changed to be just slightly above the maximum normal value in the dataset. This is a good approach if you want to keep the record without skewing averages. 
  * *Note: Always research proper statistical normalization methods before randomly adjusting values. In this dataset, the December 19th Order_Quantity could be safely adjusted from 43 to 20.*

---

## Reflection Questions

> **Question:** List the factors that could determine whether data outliers should or should not be considered in the final analysis of a dataset.
> 
> **Answer:** *[Enter your answer here]*

---

## Challenge Activity

> **Task:** Consider scenarios where data outliers could have a significant impact on the final data analysis if excluded from consideration.

---
<p align="center">
  <small>© 2017 - 2023 Cisco and/or its affiliates. All rights reserved. Cisco Public</small>
</p>
