# Revenue Cycle Audit Data Analytics — Simulated ERP Project

## Project Overview
An end-to-end audit data analytics project performed on a simulated ERP
dataset covering the revenue cycle: Sales GL, Customer Master, Product
Master, Warehouse Delivery Log, Bank Receipt Log, and AR Aging. The project
totals 20,020 sales transaction lines (20,000 unique invoices) and
THB 50,573,277,385 of net revenue (THB 54,113,406,817 gross).

## Business Scenario
A distribution/manufacturing company sells across five regions (Bangkok,
Eastern, Export, Northern, Southern) and three currencies (THB, USD, JPY),
to 50 customers across four customer types (Government, Retail,
Manufacturer, Distributor), and 30 approved products across five
categories. This project simulates a Big 4-style substantive analytics
program over that revenue cycle for a single fiscal year.

## Objectives
- Demonstrate a full revenue-cycle audit analytics workflow mapped to the
  six financial statement assertions: Occurrence, Completeness, Accuracy,
  Cut-off, Existence, and Valuation.
- Identify, quantify, and document audit findings using 100%-of-population
  data analytics rather than traditional sampling, where feasible.
- Produce professional-standard working papers, a management dashboard,
  and a risk-ranked findings summary.

## Dataset Description
| File | Description | Key Field(s) |
|---|---|---|
| 01_Customer_Master.csv | Approved customer list | Customer_ID |
| 02_Product_Master.csv | Approved product list, pricing, VAT rate | Product_Code |
| 03_Sales_GL.csv | Sales transactions (20,020 lines) | Invoice_No |
| 04_Warehouse_Log.csv | Physical delivery evidence | Delivery_Note_No |
| 05_Bank_Receipt.csv | Cash receipts sub-ledger | Invoice_No |
| 06_AR_Aging.csv | Receivables aging schedule | Invoice_No |

## Excel Skills Used
PivotTables & PivotCharts; XLOOKUP / VLOOKUP; SUMIFS / COUNTIFS /
AVERAGEIFS; COUNTIF (duplicate detection); IF / IFS / AND (conditional
flagging and aging buckets); IFERROR (safe lookup handling); SUMPRODUCT
(currency-adjusted totals and conditional averages without helper
columns); UNIQUE (distinct counts); Conditional Formatting; Slicers;
Data Validation.

## Audit Procedures Performed
1. Sales by Customer          6. Duplicate Payment Detection      11. Vouching
2. Sales by Product           7. High Value Transaction Review    12. Outstanding Accounts Receivable
3. Monthly Revenue Trend      8. Cut-off Testing                  13. AR Aging Analysis
4. Total Revenue KPI          9. Subsequent Receipt Testing        14. Customer Concentration Analysis
5. Duplicate Invoice Detection 10. Tracing                         15. Revenue Trend Analysis

## Dashboard Overview
A single-page dashboard with 6 KPI cards (Total Revenue, Total Invoices,
Total Customers, Outstanding AR, Duplicate Invoices, Duplicate Payments),
3 middle-section charts (Monthly Revenue Trend, Sales by Customer, Sales
by Product), and 3 bottom-section exception views (High Value
Transactions, Payment Status/AR Aging, Audit Findings Summary), with
Region and Customer_Type slicers connected across all charts.

## Key Audit Findings
| # | Finding | Risk | Amount (THB) |
|---|---|---|---|
| 1 | Customer concentration driven by FX/pricing translation issue | High | 86.1% of net revenue affected |
| 2 | Cut-off error at fiscal year-end (Dec invoice / Jan delivery) | High | 410,038,753 |
| 3 | Receivables aged over 90 days | High | 751,200,000 (approx.) |
| 4 | Ghost/unauthorized customer name on valid Customer_ID | High | 1,927,044 |
| 5 | Warehouse deliveries with no corresponding invoice | High | 5,252,000 (estimated) |
| 6 | Invalid product code (PROD-999) | Medium | 1,815,697 |
| 7 | Duplicate invoices | Medium | 8,030,871 |
| 8 | Duplicate bank receipts | Medium | 10 transactions |
| 9 | High-value/bulk transactions (qty > 1,000 units) | Low-Medium | 3,671,517,936 (7.3% of revenue) |

## Working Papers
Ten working papers (WP-01 through WP-10) are documented in full
Condition–Criteria–Cause–Effect–Recommendation format, each with a
Reference, Objective, Risk, Assertion, Population, Sample Selected,
Evidence, Audit Procedure, Excel Formula Used, Actual Result, Finding,
Conclusion, and Reviewer Comment — see the accompanying working paper
file for full detail.

## Audit Assertions Tested
Occurrence · Completeness · Accuracy · Cut-off · Existence · Valuation

## Accounting Standards Applied
TFRS 15 (Revenue Recognition) · TFRS 9 (Expected Credit Loss) · TAS 21
(Foreign Currency Translation) · TSA 315 (Risk Assessment) · TSA 240
(Fraud) · TSA 520 (Analytical Procedures) · TSA 500 (Audit Evidence) ·
TSA 530 (Audit Sampling) · TSA 560 (Subsequent Events) · TSA 505
(External Confirmations) · TSA 320/450 (Materiality). See Part 5 of the
accompanying report for the full standard-by-procedure mapping and an
important note that these should be verified against official TFAC
pronouncements before reliance in a real engagement.

## Folder Structure
```
/data/                  Source CSV/XLSX extracts
/workbook/              Main analysis workbook (PivotTables, formulas)
/report/                Audit review report, working papers, dashboard design
/screenshots/           Dashboard and PivotTable screenshots (see below)
README.md
```

## Screenshots Placeholder
> Insert screenshots of: (1) the Dashboard tab, (2) the Sales by
> Customer PivotTable/chart, (3) the Duplicate Invoice / Ghost
> Customer helper-column exceptions filtered view, (4) the AR Aging
> PivotChart.

## Key Skills Demonstrated
- Assertion-based audit test design (not a checklist approach)
- 100%-of-population data analytics testing using Excel formulas
- Root-cause investigation (the FX/pricing translation finding)
- Professional working paper documentation (5C / 18-field format)
- Dashboard design for non-technical stakeholders
- Mapping of findings to accounting and auditing standards

## Future Improvements
- Extend testing with Power Query for automated data refresh
- Add direct external confirmation simulation for the largest aged
  receivables and largest high-value transactions
- Build the dashboard in Power BI for interactive, cloud-hosted access
- Incorporate prior-year comparative data once available, to support
  year-over-year analytical procedures

## Conclusion
This project demonstrates a complete, assertion-based revenue cycle
audit analytics program, from raw ERP data through Excel formulas and
PivotTables, to professional working papers, a management-ready
dashboard, and a standards-mapped findings summary — reflecting the
methodology and documentation standards expected on a real Big 4
engagement.
