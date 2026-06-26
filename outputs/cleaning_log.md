# Data Cleaning Log

## Overview
This document summarises the data cleaning, validation, and business rule implementation carried out on the retail order dataset.

---

## Issues Found
The following issues were identified during the data review process:

* Extra spaces present in text fields
* Inconsistent text capitalisation across records
* Missing Region values
* Missing Ship Mode values
* Missing Discount values
* Invalid Discount values
* Inconsistent Order Status entries
* Invalid Ship Dates
* Exact duplicate records
* Duplicate Order IDs
* Revenue calculation inconsistencies
* Revenue outliers

---

## Cleaning Actions Performed
The following cleaning steps were completed:

* Leading and trailing spaces removed using TRIM
* Text values standardised using Find & Replace and formatting functions
* Date formats brought to a consistent standard
* Shipping Delay calculated and added as a derived field
* Missing Region values filled with Unknown
* Missing Ship Mode values filled with Unknown
* Discount values standardised across records
* Calculated Sales and Profit columns created
* Profit Margin calculated and added
* Order Month and Order Year extracted as separate fields
* Data Quality Flag created for each record
* Exact duplicate rows removed
* Duplicate Order IDs containing conflicting information flagged
* Revenue outliers reviewed without removing valid business records

---

## Business Rules Applied
The following business rules were put into effect during cleaning:

* Missing Region → Unknown
* Missing Ship Mode → Unknown
* Missing Discount → Zero when other sales fields were valid
* Negative Discount → Invalid
* Discount exceeding the allowed range → Invalid
* Ship Date earlier than Order Date → Invalid Shipping Record
* Cancelled Orders excluded from completed sales analysis
* Failed Payments excluded from completed sales analysis
* Refunded Orders summarised separately

---

## Calculated Columns Created
The following derived fields were added to the dataset:

* cleaned_discount
* calculated_sales
* calculated_profit
* profit_margin
* shipping_delay_days
* order_month
* order_year
* data_quality_flag

---

## Duplicate Handling

* Exact duplicate rows were identified and removed from the dataset.
* Duplicate Order IDs with conflicting information were retained.
* Conflicting records were flagged for manual review rather than deleted.

---

## Records Removed

* Exact duplicate rows were removed.
* No conflicting duplicate business records were deleted.

---

## Records Flagged
The following record types were flagged during the cleaning process:

* Invalid discount values
* Invalid shipping records
* Duplicate Order IDs
* Revenue calculation mismatches
* General data quality warnings

---

## Assumptions

* Unknown was considered an acceptable replacement for missing Region and Ship Mode values.
* Missing discounts were set to zero only where business calculations remained valid and consistent.
* Revenue outliers were kept in the dataset as they may represent legitimate high-value transactions.

---

## Limitations

* The cleaning process was based entirely on the provided dataset.
* Business rules were applied in accordance with assignment requirements.
* Certain conflicting duplicate records will require manual business verification before any deletion decisions are made.

---

## Conclusion
The cleaned dataset is consistent, validated, and ready for business reporting purposes. All significant data quality issues have been resolved, and records requiring further manual verification have been clearly documented for review.
