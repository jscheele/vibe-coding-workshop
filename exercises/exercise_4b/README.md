# Exercise 4B — Data Transformation & Reporting
**Time:** 20 minutes  |  **Dataset:** `data/transactions_clean.csv` (your output from 4A)

## Your task
Transform the clean data into business-ready reports.

## Core tasks
1. Compute **total and average transaction amount by customer segment** using `.groupby().agg()`
2. Add a `high_value` boolean column — `True` where `amount > 10000`
3. Export a summary table to `summary_report.csv`

## Extension (Intermediate / Advanced)
4. Use `pd.ExcelWriter` to produce `transaction_report.xlsx` with two sheets:
   - Sheet 1: `Segment Summary`
   - Sheet 2: `Flagged Transactions` (only rows where `high_value` is True)
5. Add a third sheet: `Branch Breakdown` — count of high-value transactions per branch
6. **Advanced bonus**: apply red fill to flagged rows using `openpyxl` styles

## Prompt tip
Include the column names and expected output format in your prompt.
Tell Copilot exactly what libraries to use.
