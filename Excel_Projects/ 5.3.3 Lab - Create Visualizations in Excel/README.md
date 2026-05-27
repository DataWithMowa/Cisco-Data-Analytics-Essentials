# Lab - Create Visualizations in Excel

## Objectives
In this lab, you will create charts to visualize data in Microsoft Excel.
* **Part 1:** Creating a Line Chart
* **Part 2:** Creating a Column Chart
* **Part 3:** Creating a Pie Chart

## Background / Scenario
Data visualization assists with the analysis and interpretation of data by graphically presenting relationships, trends, and inferences that cannot always be clearly derived by examining the raw text and numeric values in a dataset.

This lab uses sample datasets to demonstrate three visualizations of that data.

## Required Resources
* Mobile device or PC/laptop with a browser
* Microsoft 365 Excel online
* Internet access

> **Note:** The precise steps to format and manipulate data in Excel can vary between platforms and versions. The instructions in this lab are based on the free version of Excel available from *Office.com* and may have to be modified to match the user’s platform, software, or version to achieve the results shown in this lab.

---

## Part 1: Creating a Line Chart
This chart will display the Profit and Revenue for the years 2017, 2018, 2019, 2020, and 2021.

### Step 1: Download the data file
Download the sample file `Bike Sales_Visualizations_Lab.xlsx` to your OneDrive. Open the downloaded file in MS 365 Excel. This workbook contains four worksheets that each will be used separately throughout this lab.

### Step 2: Insert the line chart
1. Select the **Revenue and Profit by Year** worksheet. The worksheet contains the profit and the revenue totals for each of the years 2017, 2018, 2019, 2020, and 2021.
2. Select the data in cells **A3 through to C8**.
3. From the **Insert** menu, expand the ribbon using the down arrow on the right side of the ribbon, click the **Line chart** tool, then select **Line with Markers** (bottom left option).
   * *This creates a line chart with an x-axis showing the years, and a y-axis displaying dollar amounts.*

### Step 3: Format the chart
To improve the clarity of the chart, change the vertical axis to display USD currency.

* **Format the Vertical Axis:**
  1. Right-click on the chart and select **Format**. The *Chart Format* window pane opens on the right of the worksheet.
  2. Expand the options for the **Vertical Axis**.
  3. In the **Number Format** section, change *Category* to **Currency** and change *Decimal places* to **0**.

* **Add a Chart Title:**
  1. In the *Chart Format* window pane, change the **Chart Title** option switch to the **ON** position (if it is not already) and expand the Chart Title options.
  2. Change the Chart Title to `"Revenue vs. Profits"`.
  3. Keep the *Title Position* at the default, which is **Above**.

* **Change the Legend Names:**
  1. Select cell **B3** and change the column name to `Annual Profit`.
  2. Select cell **C3** and change the column name to `Annual Revenue`.
  3. *The legend names at the bottom of the chart should change automatically to match the column names.*

* **Reposition the Legend:**
  1. Right-click on the chart to bring up the *Chart Format* window pane.
  2. Expand the options for **Legend**.
  3. Change the *Position* option to **Right**.

* **Add Axis Titles:**
  1. If necessary, right-click on the chart to bring up the *Chart Format* window pane.
  2. Expand the **Horizontal Axis** options.
  3. Scroll down to the *Axis Title* and move the switch to the **ON** position.
  4. Add an axis title of `"Year"`.
  5. Expand the options for the **Vertical Axis**.
  6. Scroll down to the *Axis Title* and move the switch to the **ON** position.
  7. Add an axis title of `"US Dollars"`.

*(The finished chart should appear as shown in your lab manual).*

---

## Part 2: Creating a Column Chart

### Step 1: Insert the Column Chart
1. Select the **Product Revenue by Country** worksheet. The worksheet contains the revenue totals for each product category by country.
2. Select the data in cells **A3 through to E10**.
3. From the **Insert** menu, click the **Column chart** tool, then select the **Stacked Column** (middle option).
   * *This creates a column chart with an x-axis showing the country, and a y-axis showing dollar amounts.*

### Step 2: Format the chart
Using the same methods used for the line chart in Part 1, perform the following formatting changes to the chart:
* Give the chart a title of `"Product Revenue by Country"`.
* Change the vertical axis **Number Format** to **Currency** and the **Decimal Places** to **0**.
* Change the *Position* of the **Legend** to the **Right**.
* Add a horizontal **Axis Title** of `"Country"`.
* Add a vertical **Axis Title** of `"US dollars"`.

*(Once completed, the chart should appear as shown in your lab manual).*

---

## Part 3: Creating a Pie Chart

### Step 1: Insert the Pie Chart
1. Select the **Revenue by Age Group** worksheet. The worksheet contains the revenue totals for each product category.
2. Select the data in cells **A3 through to B7**.
3. From the **Insert** menu, click the **Pie chart** tool, then select the **2D-Pie** (top option).
   * *This creates a pie chart with each age group represented by an area on the chart representative of the revenue for that group.*

### Step 2: Format the chart
Using the same methods used previously for the line and column charts, make the following format changes:
* Give the chart a title of `"Revenue Comparison by Age Group"`.
* Change the *Position* of the **Legend** to the **Right**.
* **Add Data Labels to the chart area:**
  1. In the *Chart Format* window, expand the options for Series `"Total"`.
  2. Expand the options for **Data Labels**.
  3. Check the boxes for **Category Name** and **Percentage**.

*(Once completed, the chart should appear as shown in your lab manual).*

---

## Reflection Questions
Review each of the datasets given in this lab and select different options for each chart. Consider if the visualization of the data is enhanced, or not, with these different options.

### Answer Area
> *Answers will vary based on user exploration.*

---

## Challenge Activity
Explore the possibilities of using other datasets to produce different visualization charts.

---
<p align="center">
  <small>© 2017 - 2023 Cisco and/or its affiliates. All rights reserved. Cisco Public</small>
</p>
