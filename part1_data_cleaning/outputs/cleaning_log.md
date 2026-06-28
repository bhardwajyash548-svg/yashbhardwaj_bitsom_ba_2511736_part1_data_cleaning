# Cleaning Log

## Project

Business Data Cleaning, Validation and Excel Reporting

## Issues Found

The raw dataset contained several data quality issues:

* Inconsistent text formatting in customer, region, state, city, category and ship mode fields.
* Leading and trailing spaces in text columns.
* Multiple date formats in order_date and ship_date columns.
* Missing values in region, ship mode and discount fields.
* Negative discount values.
* Ship dates occurring before order dates.
* Invalid shipping delay calculations due to incorrect dates.
* Cancelled and returned orders mixed with completed orders.

---

## Cleaning Actions Performed

### Text Cleaning

The following columns were standardized:

* customer_name
* segment
* region
* state
* city
* category
* sub_category
* ship_mode
* payment_status
* order_status

Cleaning techniques used:

* TRIM
* Find and Replace
* Standardized capitalization
* Removed extra spaces
* Corrected inconsistent category names

---

### Date Cleaning

* Converted multiple date formats into a standardized format.
* Checked for missing dates.
* Checked for invalid dates.
* Identified ship dates earlier than order dates.
* Created the `shipping_delay_days` column.

---

### Missing Value Handling

* Missing region values were replaced with `Unknown`.
* Missing ship mode values were replaced with `Unknown`.
* Missing discount values were replaced with `0` when other sales information was available.

---

### Duplicate Handling

* Checked for exact duplicate rows.
* Checked for duplicate order IDs with conflicting information.
* Conflicting records were flagged for review instead of being deleted.

---

### Business Rule Validation

The following business rules were applied:

* Cancelled orders were excluded from completed sales summaries.
* Failed payment records were excluded from completed sales summaries.
* Returned and refunded orders were tracked separately.
* Negative discount values were flagged as invalid.
* Ship dates earlier than order dates were marked as invalid shipping records.

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

## Records Removed

* No records were removed automatically.
* Invalid records were flagged for manual review.

---

## Records Flagged

The following records were flagged:

* Invalid discount records
* Invalid shipping records
* Missing value records
* Business rule violations

---

## Assumptions Made

* Missing region values were assumed as `Unknown`.
* Missing ship mode values were assumed as `Unknown`.
* Missing discounts were treated as `0` where appropriate.
* Date values were converted into a single standard format.

---

## Limitations

* Some business rules required assumptions due to incomplete information.
* Date corrections were based on the available dataset values.
* Manual review may still be required for some flagged records.

---

## Final Outcome

The dataset was transformed into a clean, validated and analysis-ready dataset suitable for reporting and business decision making.

