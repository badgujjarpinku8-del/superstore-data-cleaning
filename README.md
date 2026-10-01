# Superstore Data Cleaning and Preprocessing

## Project Overview

This project focuses on cleaning and preprocessing the **Sample
Superstore dataset** so that the data is ready for reliable analysis.

The project was completed as part of a Data Analytics task focused on
identifying common data-quality issues such as missing values, duplicate
records, inconsistent formatting, incorrect data types, and invalid
values.

## Objectives

-   Inspect the raw Superstore dataset before making changes
-   Identify missing values and duplicate records
-   Standardize text formatting and date formats
-   Validate numerical columns and data types
-   Check date consistency
-   Validate relationships between the Orders, People, and Returns
    sheets
-   Create a cleaned Excel dataset
-   Maintain a change log documenting the cleaning process
-   Re-run validation checks after cleaning

## Dataset

The workbook contains three main sheets:

-   **Orders** --- sales transactions and order information
-   **People** --- regional manager information
-   **Returns** --- returned order information

The Orders sheet contains **10,194 records and 21 columns**.

## Data Cleaning Performed

### 1. Missing Values

Missing-value checks were performed across the workbook.

**Result:** No missing cells were found in the checked sheets.

### 2. Duplicate Records

Exact duplicate rows were checked.

**Result:** No exact duplicate rows were found.

> Note: Duplicate `Order ID` values were not removed because a single
> order can contain multiple products or line items.

### 3. Text Formatting

Text fields were checked and leading/trailing whitespace was removed
where applicable.

This helps prevent issues such as:

``` text
"Consumer "
" Consumer"
"Consumer"
```

being treated as different values.

### 4. Date Formatting

The following fields were standardized as date values:

-   `Order Date`
-   `Ship Date`

The relationship between the two dates was also validated.

### 5. Numerical Validation

The following fields were validated as numeric data:

-   `Sales`
-   `Quantity`
-   `Discount`
-   `Profit`

The following checks were performed:

-   Quantity greater than 0
-   Sales greater than 0
-   Discount between 0 and 1

No invalid records were found.

### 6. Cross-Sheet Validation

Relationships between sheets were checked.

-   Return `Order ID` values were checked against the Orders sheet.
-   Regions in the Orders sheet were checked against the People sheet.

No unmatched records were found.

## Final Deliverables

The cleaned workbook contains:

``` text
cleaned_superstore_excel.xlsx
│
├── Orders
├── People
├── Returns
├── Change Log
└── Cleaning Summary
```

The **Change Log** documents the quality checks and cleaning actions
performed.

The **Cleaning Summary** provides before-and-after validation results.

## Tools Used

-   Microsoft Excel
-   Python
-   Pandas

## Project Workflow

``` text
Raw Dataset
     ↓
Initial Data Inspection
     ↓
Missing Value Check
     ↓
Duplicate Check
     ↓
Text & Format Validation
     ↓
Date Validation
     ↓
Numerical Validation
     ↓
Cross-Sheet Validation
     ↓
Cleaning & Standardization
     ↓
Final Validation
     ↓
Cleaned Dataset
```

## Key Findings

The dataset was already relatively clean. No missing values, exact
duplicate rows, invalid quantities, invalid sales values, invalid
discounts, invalid date relationships, or unmatched cross-sheet keys
were found during validation.

Because the purpose of data cleaning is to improve data quality rather
than make unnecessary changes, values were not artificially changed when
no issue was present.

## Repository Structure

``` text
superstore-data-cleaning/
│
├── README.md
├── data/
│   └── cleaned_superstore_excel.xlsx
│
├── notebooks/
│   └── data_cleaning.ipynb
```

## Conclusion

The Superstore dataset was systematically inspected, cleaned,
standardized, and validated. The final Excel workbook is structured for
further analysis and includes documentation of the cleaning process.

------------------------------------------------------------------------

**Project:** Superstore Data Cleaning and Preprocessing\
**Focus:** Data Quality and Preparation\
**Tools:** Excel, Python, Pandas

