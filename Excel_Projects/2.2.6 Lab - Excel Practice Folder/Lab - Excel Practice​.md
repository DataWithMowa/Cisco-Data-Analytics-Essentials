# Lab - Excel Practice

## Objectives
* **Part 1:** Launch Excel and Enter Data into a Worksheet
* **Part 2:** Add Formulas and Functions
* **Part 3:** Save the Workbook and Close Excel

## Required Resources
* Mobile device or PC/laptop with an internet connection and Microsoft Excel or similar spreadsheet program

**Note:** The precise steps to format and manipulate data in Excel can vary between platforms and versions. The instructions in this lab are based on the free version of Excel available from Office.com and may have to be modified to match the user’s platform, software, or version to achieve the results shown in this lab.

## Introduction
In this lab you will practice what you have learned so far about Excel.

## Part 1: Launch Excel and Enter Data into a Worksheet

### Step 1: Launch Excel and Start Worksheet
1. Launch Excel and open a blank worksheet.
2. Rename the worksheet **“Sales Data”**.

### Step 2: Add column headers
1. Enter the following column headers in **Row 1** of the worksheet in order from **A1** to **J1**:
   * Date
   * Country
   * State
   * Product
   * Order_Quantity
   * Unit_Cost
   * Unit_Price
   * Total_Cost
   * Revenue
   * Profit
2. Fill out the data for the first seven columns as shown below. Expand the width of the columns as needed so that all of the text in each cell is visible.
CHECK EXCEL FILE ATTACHED TO SEE THE RESULT

### Step 2: Add column headers (Continued)
c. Perform the following formatting operations on the cells in the worksheet:
1. **Boldface** the column headers in **Row 1**.
2. **Center** the column headers horizontally in the **Row 1** cells.
3. Change the number format of the **Unit_Cost**, **Unit_Price**, **Total_Cost**, **Revenue**, and **Profit** columns to **Currency**.

---

## Part 2: Add Formulas and Functions

### Step 1: Using Formulas

1. In cell **H2** under **Total_Cost**, write a formula that calculates the total cost of the products sold.
   * The formula should multiply the **Order_Quantity** by the **Unit_Cost**.
   * *Example:* `=E2*F2`
   * This will calculate the total cost of the units sold.
2. Copy and paste the formula from cell **H2** to cells **H3** through **H6**.

3. In cell **I2** under **Revenue**, write a formula that calculates the total revenue of the products sold.
   * The formula should multiply the **Order_Quantity** by the **Unit_Price**.
   * *Example:* `=E2*G2`
   * This will calculate the revenue received from sales.
4. Copy and paste the formula from cell **I2** to cells **I3** through **I6**.

5. In cell **J2** under **Profit**, write a formula that calculates the profits made from the sale of each item.
   * The formula should subtract the **Total_Cost** from the **Revenue**.
   * *Example:* `=I2-H2`
   * This will calculate the profit made from sales.
6. Copy and paste the formula from cell **J2** to cells **J3** through **J6**.

The worksheet should now appear as shown below:
CHECK EXCEL FILE ATTACHED TO SEE THE RESULT.

### Step 2: Using Functions

1. **Underline** the data in cells **I6** and **J6**.
2. In cell **H7**, enter the text: `Total =`.
3. In cell **I7**, use the **Sum function** to calculate the total revenue from all sales.
   * *Example:* `=SUM(I2:I6)`
4. In cell **J7**, use the **Sum function** to calculate the total profits from all sales.
   * *Example:* `=SUM(J2:J6)`
5. **Boldface** cells **H7**, **I7**, and **J7**.

Columns H, I, and J should now appear as follows:
CHECK EXCEL FILE ATTACHED TO SEE THE RESULT.

Part 3: Save the Workbook and Close Excel
Step 1: Save the Workbook as Bike_Sales_Data and then close Excel.
