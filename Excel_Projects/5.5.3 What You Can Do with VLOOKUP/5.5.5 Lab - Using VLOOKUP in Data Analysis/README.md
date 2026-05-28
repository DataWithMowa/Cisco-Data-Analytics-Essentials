# Lab - Using VLOOKUP in Data Analysis​

## Objectives
In this lab, you will use the VLOOKUP function in Microsoft Excel to:
* **Part 1:** Initial Examination of a Large Dataset
* **Part 2:** Apply the VLOOKUP Function

## Background / Scenario
Searching for a single data record from a very large dataset for analysis usually requires the application of specific search functions to facilitate locating and extracting the information required. In this lab, the Excel VLOOKUP function will be used to locate information from a large dataset.

## Required Resources
* Mobile device or PC/laptop with a browser, MS 365 Excel online, and an Internet connection

> **Note:** The precise steps to format and combine or split data in Excel can vary between platforms and versions. The instructions in this lab are based on the free version of Excel available from Office.com and may have to be modified to match the platform or version used to achieve the results shown in this lab.

---

## Instructions

### Part 1: Initial Examination of a Large Dataset

#### Step 1: Download the data file.
* Download the sample workbook file `Bike Sales_VLOOKUP.xlsx` and save it to your OneDrive.
* Open the downloaded file in **MS 365 Excel online**. Adjust the column widths such that the data is visible.
* **Freeze the top (Heading) row** so it remains visible as you scroll through the many thousands of entries. Click **View > Freeze Panes** and select **Freeze Top Row**.

#### Step 2: Examine the data.
* Scroll through and examine the data in the worksheet. The worksheet contains bikes sales data for the 4th quarter of 2021 which is 752 rows of data.
* As can be seen, even if the data is sorted by Sales_Order # or Date, the size of the dataset means that manually searching for information about a specific sale would be time consuming and perhaps prone to error.
* To facilitate searching, this lab will use VLOOKUP to display the Sales_Order Number and Product of a particular sale.
* An important requirement of VLOOKUP is that the reference data must be in the leftmost (first) column of the dataset in Excel. In this lab, Sales_Order# is being used as the search reference and must be the first column (Column A in this spreadsheet).

---

### Part 2: Apply the VLOOKUP Function

#### Step 1: Select result display area
For usability and consistency, especially with large datasets, it is best practice to select a blank area of the worksheet, or a new blank worksheet, in which to enter the search criteria and display the result.

This entry and display area may be on another worksheet within the spreadsheet; or may be enabled by using macros and forms. For this lab, the entry and display area will be on the same worksheet adjacent to the data.

The values to be used are Sales_Order#, Product, and Order_Quantity.
* In cell **U3**, enter `Sales_Order # =`
* In cell **U4**, enter `Product =`
* In cell **U5**, enter `Order_Quantity =`

#### Step 2: Create the VLOOKUP functions
* In cell V4 enter `=VLOOKUP(V3, A2:S753 ,13, FALSE)`
* In cell V5 enter `=VLOOKUP(V3, A2:S753 ,14, FALSE)`

**Where:**
* **V3** is the cell where the reference (lookup) value, the sales order number, is entered.
* **A2:S753** is full range of data across all columns and rows that will be searched.
* **13** is the index (column number) with respect to the reference column; Product is the 13th column to the right of the Sales_Order# column, column A.
* **14** is the index (column number) with respect to the reference column; Order_Quantity is the 14th column to the right of the Sales_Order# column, column A.
* **FALSE** denotes an exact match for the movie title must be found.

#### Step 3: Test the VLOOKUP functions
* Enter a Sales_Order# in cell V3 and observe the displayed Product and Order_Quantiy in cells V4 and V5.
* If you enter Sales_Order# 000261274 the returned results should be “Road-650 Red 44” for the Product and “2” for the Order_Quantity. If Excel is displaying 261274 in cell V3, enter `'000261274` into cell V3. The single quote (') forces the leading zeros in the sales order number to be included in the lookup.

#### Step 4:
* Test the VLOOKUP functions with other sales order numbers.

#### Step 5: Improve the VLOOKUP function
If a sales order number is entered that is not found in the dataset, then #N/A is displayed.
* In cell V3 enter an invalid sales order number such as `12345`
* The result in cells V4 and V5 is `#N/A`.
* This result is not very helpful to the user. A solution is to modify each VLOOKUP function.
* Change cell M4 to `= IFNA(VLOOKUP(V3, A2:S753 ,13, FALSE), "Not Found")`
* Change cell M5 to `= IFNA(VLOOKUP(V3, A2:S753 ,14, FALSE), "Not Found")`

The VLOOKUP function is enclosed within a IFNA function, which if TRUE displays the given text. An invalid sales order number should now return “Not Found”.

* Try other valid and invalid order numbers to test the VLOOKUP function.

---

## Reflection Questions
Consider searching the dataset for other information relating to a particular movie.

**1. Write a VLOOKUP function to retrieve the Cost of a particular order.**
> `= IFNA(VLOOKUP(V3, A2:S753 ,18, FALSE), "Not Found")`

**2. Write a VLOOKUP function to retrieve the Revenue of a particular order.**
> `= IFNA(VLOOKUP(V3, A2:S753 ,19, FALSE), "Not Found")`

---

## Challenge Activity
Explore the possibilities of using VLOOKUP on other datasets and how useful this would be in analyzing the data. Consider what would be the reference data and the structure of the VLOOKUP function to achieve the required analysis.

---
<p align="center">
  <small>© 2017 - 2023 Cisco and/or its affiliates. All rights reserved. Cisco Public</small>
</p>
