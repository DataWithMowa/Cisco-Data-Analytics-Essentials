# Lab: Synchronizing Data with Workbook Links

## Background / Scenario
The bicycle shop keeps sales data in separate worksheets, one for each year. They would like you to perform data analysis on their sales records. In this lab, you will create a consolidated spreadsheet containing external links to each year’s data.

## Required Resources
*   Microsoft 365 Excel on Office.com
*   Microsoft 365 OneDrive

---

## Instructions

### Part 1: Creating External Links

#### Step 1: Open the worksheets to be linked
To work with the data from the 2021 and 2022 sales, download the Excel workbooks **BikeSales_2021.xlsx** and **BikeSales_2022.xlsx**.

1.  Sign into your Microsoft 365 account. Upload the two workbook files to your Microsoft 365 OneDrive.
2.  Open each of the workbooks in Excel online. You should see both workbooks listed on separate tabs in your browser.
3.  On a separate browser tab, open a new blank workbook in Excel. Rename the spreadsheet **BikeSales_Consolidated**.
4.  Place the cursor in the cell **A1** of the BikeSales_Consolidated spreadsheet. Type an equal sign (**=**) and then click the browser tab containing the BikeSales_2021 worksheet. A notice will appear that indicates you are setting a Workbook link.
5.  Select the data that you want to link to the BikeSales_Consolidated workbook. In this case, select all of the data by placing the cursor in cell **A1** and pressing the shortcut **CTRL-SHIFT-END** or by clicking and dragging from cell **A1** to cell **R14**.
6.  Return to the BikeSales_Consolidated workbook. The formula for the link appears in the formula bar and in cell **A1**. Press **ENTER**.
    *   *Note: If a warning appears that “External Data Connections have been disabled”, select **Enable Content** to continue.*
7.  Open a new worksheet in the BikeSales_Consolidated workbook using the **+** tab at the bottom of the window. Repeat the previous steps in this new worksheet with the 2022 Sales worksheet.
8.  The BikeSales_Consolidated workbook should now have two sheets, Sheet1 containing the 2021 sales data and Sheet2 containing the 2022 data.

---

### Part 2: Refreshing Data in Multiple Sheets
The Worksheet Links function enables you to update data when the original data changes, by refreshing the linked data.

#### Step 1: Use Excel Functions to Summarize Data from Multiple Worksheets
1.  Add a new worksheet (**Sheet3**) to the BikeSales_Consolidated workbook.
2.  In Row 1, create two column headings: **2021 Average Cost** and **2021 Average Revenue**.
3.  In Cell **A2**, type (do not copy and paste) `=AVERAGE(`. Then, with the cursor next to the open parenthesis, click on the browser tab that contains the BikeSales_2021 worksheet.
4.  Select the range of cells **Q2:Q14**. Return to the BikeSales_Consolidated workbook and press **ENTER**.

> **What is the value in Cell A2 after the spreadsheets are linked?**
> *[Answer Area]*

5.  Place the cursor in cell **B2**. Repeat the steps to return the average of 2021 revenue (Column **R** in the BikeSales_2021 Worksheet).

> **What is the value in Cell B2 after the spreadsheets are linked?**
> *[Answer Area]*

#### Step 2: Update Data in the Source Spreadsheet
Now that the spreadsheets are linked, updates to the data in the source sheet can be automatically updated in the consolidated sheet.

1.  Open the browser tab containing the **BikeSales_2021** worksheet.
2.  Update the value in cell **Q6** to be **$30,000.00**. Return to the BikeSales_Consolidated worksheet **Sheet3**.
3.  Select **Data > Workbook Links** (in the Queries & Connections section) in the tool bar. A window opens on the side of the screen with a list of workbooks linked to this worksheet.
4.  Click the circular **refresh icon** next to the BikeSales_2021.xlsx listing.

> **What happens to the average values in cell A2?**
> *[Answer Area]*

5.  Open **Sheet1** that contains the linked data from BikeSales_2021 and press the refresh button in the Workbook Links panel again.

> **What is the value in cell Q6?**
> *[Answer Area]*

---

## Reflection
**What are some situations in which you would want to use Workbook links to keep data synchronized between workbooks?**
- When managing data that is too large for a single file.

- When different departments (Sales, HR, Finance) manage their own data but you need a combined report.

- When you want to create a "Master Dashboard" without cluttering it with thousands of rows of raw data.

*[Answer Area]*
