# Prompt Cards — Exercise 4A (Beginner)

Copy each prompt into GitHub Copilot Chat. Read the output before pressing run.

---

**Plan the plan**
> Before writing any code, tell me your step-by-step plan for cleaning this dataset.
> What issues will you address, in what order? Don't write code yet.

---

**Issue 1 — Strip currency symbols from amount**
> I have a Pandas DataFrame called `df` with a column called `amount` that contains strings
> like `"$1,250.00"` and `"$80.00"`. Write Python code using pandas to strip the `$` symbol
> and commas, then convert the column to float. Store the result back in `df['amount']`.

---

**Issue 2 — Standardise mixed date formats**
> My `df['date']` column contains dates in mixed formats: some are `YYYY-MM-DD`, some are
> `DD/MM/YYYY`, and some are like `Jan 15 2024`. Write Python code using pandas to convert
> all of these to a consistent `datetime` type using `pd.to_datetime` with `errors='coerce'`.

---

**Issue 3 — Uppercase category**
> Write Python code to strip leading and trailing whitespace from `df['category']` and
> convert all values to uppercase. Store the result back in `df['category']`.

---

**Issue 4 — Remove duplicate rows**
> Write one line of Python/pandas code to remove fully duplicate rows from `df` (where all
> column values are identical). Keep the first occurrence.

---

**Issue 5 — Handle missing amounts**
> My `df['amount']` has some missing values (NaN). Write Python code to:
> (1) add a new boolean column called `flag_missing` that is True where amount is NaN;
> (2) fill the missing amount values with 0.

---

**Issue 6 — Remove sentinel values**
> Write Python code to remove all rows from `df` where `df['amount'] == -9999`.
> Use boolean indexing and reassign to `df`.

---

**Issue 7 — Strip branch whitespace**
> Write one line of Python/pandas code to strip leading and trailing whitespace from the
> `branch` column in `df`.

---

**Issue 8 — Flag invalid customer IDs**
> My `df['customer_id']` should follow the format `CUST_` followed by exactly 6 digits
> (e.g. `CUST_123456`). Write Python code to add a boolean column `flag_bad_id` that is
> True for rows that do NOT match this pattern. Use `str.match()` or `str.contains()`.
