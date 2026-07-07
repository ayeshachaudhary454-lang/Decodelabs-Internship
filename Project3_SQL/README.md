# Project 3: SQL Data Analysis 🗄️

**DecodeLabs Industrial Training Kit — Batch 2026**
**Prepared by:** Ayesha Sarwar

## Goal
Use SQL queries to extract business insights from the e-commerce dataset.

## Files
| File | Description |
|---|---|
| `Project3_SQL_AyeshaSarwar.ipynb` | Jupyter notebook with all SQL queries |
| `cleaned_dataset.csv` | Input dataset (from Project 1) |

## SQL Concepts Covered
| Concept | Purpose |
|---|---|
| SELECT | Choose specific columns to display |
| WHERE | Filter rows by condition |
| ORDER BY | Sort results ascending or descending |
| GROUP BY | Group rows into category buckets |
| HAVING | Filter after grouping |
| COUNT() | Count number of orders |
| SUM() | Calculate total revenue |
| AVG() | Calculate average order value |

## Queries Written
1. SELECT — Preview first 5 orders
2. WHERE — Filter delivered orders only
3. WHERE + ORDER BY — High value orders above 2000
4. GROUP BY + COUNT — Orders per product
5. GROUP BY + SUM + AVG — Revenue per product
6. GROUP BY + COUNT — Orders per payment method
7. GROUP BY + HAVING — Products with more than 150 orders
8. ORDER STATUS breakdown — Fulfillment performance

## Key Findings
- Returned orders had the highest count
- Laptop generated highest total revenue
- Debit Card was the most used payment method
- All SQL concepts demonstrated: SELECT, WHERE, ORDER BY, GROUP BY, HAVING, COUNT, SUM, AVG

## Tech Stack
- Python 3.11, pandas, sqlite3, Jupyter Notebook
