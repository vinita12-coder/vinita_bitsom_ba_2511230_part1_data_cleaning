# Business Data Cleaning, Validation & Excel Reporting

## Project Summary
This project centres on cleaning, validating, and preparing retail order data for business analysis. The raw dataset presented a range of issues including inconsistent text formatting, invalid dates, duplicate records, missing values, discount irregularities, calculation discrepancies, and inconsistent order status entries.

The goal was to produce a clean, analysis-ready dataset alongside validation reports and business summary dashboards built in Microsoft Excel.

---

# Dataset Description
The dataset holds order-level retail transaction records covering:

* Order ID
* Order Date
* Ship Date
* Customer Details
* Product Information
* Region and Location
* Quantity
* Unit Price
* Discount
* Sales
* Cost
* Profit
* Payment Status
* Order Status

The original dataset was retained as **raw_orders.xlsx**, while all cleaning work was carried out in **cleaned_orders.xlsx**.

---

# Tools Used

* Microsoft Excel
* Pivot Tables
* Excel Formulas
* Conditional Formatting
* Sorting & Filtering
* Data Validation

---

# Cleaning Steps Performed
The following cleaning activities were completed:

* Removed leading, trailing, and extra spaces from text fields
* Applied consistent text formatting across all relevant columns
* Corrected inconsistent category and status values
* Standardised order and ship date formats
* Built a shipping delay calculation column
* Reviewed and addressed missing values
* Filled missing Region and Ship Mode entries with **Unknown** where applicable
* Standardised discount values across records
* Created calculated sales and profit columns
* Derived profit margin for each record
* Extracted order month and order year as separate fields
* Generated a data quality flag for every record
* Identified and documented exact duplicate rows
* Flagged duplicate Order IDs with conflicting information
* Reviewed revenue calculations for consistency
* Produced business summary pivot reports

---

# Business Rules Applied
The following business rules were put in place during cleaning:

* Missing Region → Filled as **Unknown**
* Missing Ship Mode → Filled as **Unknown**
* Missing Discount → Treated as **0** when other fields were valid
* Negative Discount → Flagged as Invalid
* Discount above the valid range → Flagged as Invalid
* Ship Date before Order Date → Flagged as Invalid
* Cancelled Orders excluded from completed sales summaries
* Failed Payments excluded from completed sales summaries
* Refunded Orders analysed separately

---

# Data Quality Issues Identified
The validation process surfaced the following issues:

* Missing values across selected fields
* Exact duplicate records
* Duplicate Order IDs with conflicting information
* Invalid shipping records
* Discount inconsistencies
* Revenue outliers
* Order status inconsistencies

All identified issues were either corrected, documented, or flagged for business review.

---

# Pivot Reports Created
The project delivers the following business summary reports:

* Sales and Profit by Region
* Sales and Profit by Category & Sub-Category
* Order Count by Ship Mode
* Profit Margin by Customer Segment
* Refunded, Cancelled, and Failed Orders by Region
* Monthly Sales Trend

Several pivot tables incorporate sorting and filtering options to support more flexible business reporting.

---

# Key Business Insights

* Regional sales performance was broadly distributed across all regions.
* Technology generated the highest sales and profit figures.
* Consumer customers recorded the highest average profit margin.
* Standard Class was the most widely used shipping method.
* Business risks linked to duplicate records and invalid data were successfully identified and documented.

---

# Assumptions and Limitations

* Missing Region and Ship Mode values were replaced with **Unknown**.
* Missing discounts were set to zero only when supporting sales information was valid.
* Exact duplicate rows were removed from the dataset.
* Duplicate Order IDs with conflicting information were kept and flagged for manual business review.
* Business validation was limited to the fields available within the dataset.

---

# Screenshots Included
The repository contains the following screenshots:

* raw_data_preview.png
* cleaned_data_preview.png
* pivot_summary_1.png
* pivot_summary_2.png

---

# Conclusion
The final cleaned dataset is consistent, validated, and ready for business reporting. The generated reports deliver clear visibility into regional performance, product profitability, customer profitability, shipping behaviour, and overall data quality.
