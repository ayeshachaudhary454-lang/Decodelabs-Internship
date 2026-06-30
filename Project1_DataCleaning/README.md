# Project 1: Data Cleaning & Preparation 🧹

> **DecodeLabs Industrial Training Kit — Batch 2026**
> Prepared by **Ayesha Sarwar**

A data cleaning pipeline built in Python (pandas) that transforms a raw, 1,200-row e-commerce orders dataset into a validated, analysis-ready "gold standard" dataset — handling missing values, duplicate records, and inconsistent formatting.

---

## 📁 Repository Contents

| File | Description |
|---|---|
| `Project1_DataCleaning_AyeshaSarwar.ipynb` | Jupyter notebook with the full cleaning workflow, documented step-by-step |
| `Dataset for Data Analytics - Sheet1.csv` | Raw input dataset (1,200 orders, 14 columns) |
| `cleaned_dataset.csv` | Final cleaned output dataset |
| `README.md` | This file |

---

## 🎯 Project Goal

Clean a raw dataset by:
- Identifying and handling missing/null values
- Detecting and removing duplicate records
- Correcting inconsistent formats (dates, text, numbers)
- Proving data integrity via a validation gate (0% error rate on unique IDs and date formats)

---

## 🛠 Tech Stack

- Python 3.11
- pandas
- NumPy
- Jupyter Notebook

---

## 🔍 Methodology

### 1. Initial Inspection
Loaded the dataset and reviewed its shape, column types, and structure (`df.info()`, `df.head()`).

### 2. Phase 1 — Strategic Imputation
- Found 309 missing values, all in the `CouponCode` column.
- Since a blank coupon code represents *no coupon applied* (not unknown data), missing values were filled with `'NONE'` instead of being dropped — preserving all 1,200 records.

### 3. Phase 2 — The Integrity Audit
- Checked for exact duplicate rows and duplicate `OrderID` values (the dataset's unique key).
- **Result:** 0 duplicates found.

### 4. Phase 3 — Speak One Language
Standardized formatting across the dataset:
- **Dates** → ISO 8601 (`YYYY-MM-DD`)
- **Text fields** (`Product`, `ShippingAddress`, `PaymentMethod`, `OrderStatus`, `ReferralSource`, `CouponCode`) → trimmed whitespace, standardized casing
- **Currency fields** (`UnitPrice`, `TotalPrice`) → rounded to 2 decimal places

### 5. Cross-Field Validation
Verified `TotalPrice = Quantity × UnitPrice` across all records to catch hidden calculation errors.
**Result:** 0 mismatches.

### 6. Validation Gate ✅
Final proof of data quality:

| Check | Result |
|---|---|
| Duplicate OrderIDs | 0 → **PASS** |
| Incorrectly formatted dates | 0 → **PASS** |
| Remaining null values | 0 → **PASS** |

---

## 🚀 How to Run

\`\`\`bash
# Clone the repo
git clone <your-repo-url>
cd <repo-folder>

# Install dependencies
pip install pandas numpy jupyter

# Launch Jupyter
jupyter notebook
\`\`\`

Open `Project1_DataCleaning_AyeshaSarwar.ipynb` and run all cells (**Cell → Run All**). The cleaned dataset will be saved as `cleaned_dataset.csv` in the same directory.

---

## 📊 Results Summary

| Metric | Before | After |
|---|---|---|
| Rows | 1,200 | 1,200 |
| Missing values | 309 (CouponCode) | 0 |
| Duplicate OrderIDs | 0 | 0 |
| Date format consistency | N/A | 100% ISO 8601 |
| Price calculation accuracy | N/A | 100% verified |

---

## 📬 Contact

**Ayesha Sarwar**
Part of the DecodeLabs Industrial Training Kit, Batch 2026.
