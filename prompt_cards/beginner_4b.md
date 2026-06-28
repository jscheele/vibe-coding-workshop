# Prompt Cards — Exercise 4B (Beginner)

Copy each prompt into GitHub Copilot Chat. Read the output before pressing run.

---

**Plan the plan**
> Before writing any code, tell me your step-by-step plan for transforming this clean
> transaction dataset into business-ready reports. Don't write code yet.

---

**Task 1 — Summary by segment**
> I have a Pandas DataFrame called `df` with columns including `segment` and `amount`.
> Write Python code using `.groupby().agg()` to compute the total and average `amount`
> for each `segment`. Store the result in a new DataFrame called `summary`.

---

**Task 2 — Flag high-value transactions**
> Write Python code to add a boolean column called `high_value` to `df` that is `True`
> where `amount` is greater than 10000, and `False` otherwise.

---

**Task 3 — Export summary to CSV**
> Write one line of Python/pandas code to export the `summary` DataFrame to a CSV file
> called `summary_report.csv`, without the index column.

---

**Extension — Multi-sheet Excel report**
> Using `pandas` and `pd.ExcelWriter` with the `openpyxl` engine, write Python code to
> create a file called `transaction_report.xlsx` with two sheets: `Segment Summary`
> (the `summary` DataFrame) and `Flagged Transactions` (only rows from `df` where
> `high_value` is True).

---

**Extension — Branch breakdown sheet**
> Add a third sheet called `Branch Breakdown` to the same Excel file, containing a count
> of high-value transactions per `branch`.
