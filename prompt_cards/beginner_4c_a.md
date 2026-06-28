# Prompt Cards — Exercise 4C, Option A: Loan Eligibility Checker (Beginner)

Copy each prompt into GitHub Copilot Chat. Read the output before pressing run.

---

**Plan the plan**
> Before writing any code, tell me your step-by-step plan for applying these three
> lending rules to each row of a loan applicant DataFrame. Don't write code yet.
> Rule 1: annual_income / 12 >= 3 * monthly_repayment, else DECLINED.
> Rule 2: credit_score >= 650, else REFERRED.
> Rule 3: loan_amount / property_value <= 0.80, else DECLINED.

---

**Task 1 — Write the decision function**
> I have a Pandas DataFrame called `df` with columns `annual_income`, `credit_score`,
> `loan_amount`, `property_value`, and `monthly_repayment`. Write a Python function
> `decide(row)` that returns a tuple `(decision, reason)` where `decision` is one of
> `"APPROVED"`, `"REFERRED"`, `"DECLINED"` based on these rules, checked in this order:
> (1) if income is insufficient or LTV is too high, DECLINED;
> (2) else if credit score is below 650, REFERRED;
> (3) else APPROVED.
> `reason` should be a short string explaining which rule(s) failed, or "all checks passed".

---

**Task 2 — Apply it to every row**
> Write Python code using `df.apply()` to call `decide()` on every row of `df` and store
> the results in two new columns: `decision` and `reason`.

---

**Task 3 — Export results**
> Write Python code to export `applicant_id`, `name`, `decision`, and `reason` from `df`
> to a CSV file called `loan_decisions.csv`, without the index column.

---

**Extension — Configurable thresholds**
> Refactor the code so the credit score threshold (650), LTV threshold (0.80), and income
> multiplier (3) are defined as variables at the top of the script instead of hardcoded
> inside the function.

---

**Extension — Summary counts**
> Write Python code to print how many applicants fall into each `decision` category
> using `value_counts()`.
