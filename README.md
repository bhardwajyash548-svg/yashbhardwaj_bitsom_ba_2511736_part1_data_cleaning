# yashbhardwaj_bitsom_ba_2511736_part1_data_cleaning

# Part 1: Business Data Cleaning, Validation & Excel Reporting

## Problem Summary

A retail company exported order-level sales data from multiple internal systems. The dataset contained multiple data quality issues such as inconsistent text formatting, missing values, invalid discounts, duplicate records, and inconsistent date formats.

The objective of this project was to clean, validate, and prepare the dataset for business analysis and reporting using Excel.

---

## Dataset Description

Dataset used:

* `raw_orders.xlsx`

Cleaned dataset generated:

* `cleaned_orders.xlsx`

The dataset contains information related to:

* Orders
* Customers
* Sales
* Profit
* Discounts
* Shipping
* Payment Status
* Order Status

---

## Tools Used

* Microsoft Excel Online
* Pivot Tables
* Excel Formulas
* Data Validation Techniques

---

## Cleaning Steps Performed

### Text Cleaning

The following fields were standardized:

* Customer Name
* Segment
* Region
* State
* City
* Category
* Sub Category
* Ship Mode
* Payment Status
* Order Status

Techniques used:

* TRIM
* Find and Replace
* Standardization of text values

---

### Date Cleaning

* Standardized multiple date formats into a consistent format.
* Identified invalid dates.
* Checked for missing dates.
* Flagged ship dates earlier than order dates.
* Created shipping delay calculations.

---

### Missing Value Handling

* Missing Region values were replaced with `Unknown`.
* Missing Ship Mode values were replaced with `Unknown`.
* Missing Discount values were replaced with `0` when valid.

---

### Duplicate Handling

* Checked for exact duplicate records.
* Checked for duplicate Order IDs.
* Flagged conflicting records for review.

---

## Business Rules Applied

* Cancelled orders were excluded from completed sales summaries.
* Failed payment records were excluded from completed sales summaries.
* Refunded orders were summarized separately.
* Negative discounts were marked invalid.
* Invalid shipping records were flagged.

---

## Calculated Columns Created

The following calculated fields were added:

* cleaned_discount
* calculated_sales
* calculated_profit
* profit_margin
* shipping_delay_days
* order_month
* order_year
* data_quality_flag

---

## Data Quality Issues Found

The following issues were identified:

* Missing values
* Inconsistent date formats
* Invalid discounts
* Invalid shipping records
* Business rule violations

All issues were either corrected or flagged for further review.

---

## Pivot Reports Created

The following business reports were created:

1. Sales and Profit by Region
2. Sales and Profit by Category and Sub Category
3. Order Count by Ship Mode
4. Profit Margin by Customer Segment
5. Refunded and Cancelled Orders by Region
6. Monthly Sales Trend

---

## Key Business Insights

* West region generated the highest sales contribution.
* Some records contained invalid shipping dates.
* Cancelled and refunded orders impacted revenue performance.
* Profitability varied significantly across customer segments.
* Missing values were limited and manageable after cleaning.

---

## Assumptions

* Missing Region values were replaced with `Unknown`.
* Missing Ship Mode values were replaced with `Unknown`.
* Missing Discount values were treated as `0` when applicable.
* Invalid records were flagged instead of deleted.

---

## Limitations

* Some business assumptions were required due to missing information.
* Manual validation may still be required for flagged records.
* Results depend on the quality of source system data.

---

## Repository Structure

```text
part1_data_cleaning/
├── data/
│   ├── raw_orders.xlsx
│   └── cleaned_orders.xlsx
├── outputs/
│   ├── data_quality_report.xlsx
│   ├── pivot_summary.xlsx
│   └── cleaning_log.md
├── screenshots/
│   ├── raw_data_preview.png
│   ├── cleaned_data_preview.png
│   ├── pivot_summary_1.png
│   └── pivot_summary_2.png
└── README.md
```

---

## Screenshots Included

* Raw Data Preview
* Cleaned Data Preview
* Pivot Summary 1
* Pivot Summary 2

---

## Final Outcome

The raw retail dataset was successfully transformed into a clean, validated, and analysis-ready dataset suitable for business reporting and decision-making.
