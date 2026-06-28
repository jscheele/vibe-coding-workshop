# Prompt Cards — Exercise 4C, Option B: Transaction Alert Generator (Beginner)

Copy each prompt into GitHub Copilot Chat. Read the output before pressing run.

---

**Plan the plan**
> Before writing any code, tell me your step-by-step plan for flagging transactions
> against three alert rules. Don't write code yet.
> Rule 1 (HIGH_VALUE): amount > 10000.
> Rule 2 (CASH_LIMIT): category == 'CASH_WITHDRAWAL' and amount > 5000.
> Rule 3 (DUPLICATE_SUSPECT): same customer_id, amount, and date as another row.

---

**Task 1 — Flag each rule separately**
> I have a Pandas DataFrame called `df` with columns `date`, `customer_id`, `amount`,
> `category`, and `branch`. Write Python code to create three boolean columns:
> `is_high_value` (amount > 10000), `is_cash_limit` (category is 'CASH_WITHDRAWAL' and
> amount > 5000), and `is_duplicate_suspect` (rows sharing the same `customer_id`,
> `amount`, and `date` as at least one other row — use `duplicated()` with `keep=False`
> on those three columns).

---

**Task 2 — Build the alert_type column**
> Write Python code that creates a new column `alert_type` listing which of the three
> rules a row matches (e.g. `"HIGH_VALUE"`, or `"HIGH_VALUE, CASH_LIMIT"` if more than
> one applies), and filters `df` down to only the rows that match at least one rule.

---

**Task 3 — Add recommended actions and export**
> Add a `recommended_action` column with a short instruction per alert type (e.g.
> "Review with customer" for HIGH_VALUE, "Verify cash source" for CASH_LIMIT,
> "Check for duplicate posting" for DUPLICATE_SUSPECT). Then export `date`, `customer_id`,
> `amount`, `category`, `branch`, `alert_type`, `recommended_action` to
> `flagged_transactions.csv`, sorted by `amount` descending.

---

**Extension — Summary by alert type**
> Write Python code to print a count of flagged transactions per `alert_type`.
