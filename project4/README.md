# Project 4: Data Visualization — E-Commerce Sales Insights

## Overview
This project is part of the DecodeLabs Data Analytics Industrial Training Kit
(Optional Mastery Phase: Data Visualization). It applies the **Architect → Editor →
Storyteller** framework to move from raw e-commerce order data to boardroom-ready,
decision-driving charts.

The goal isn't just "making pretty pictures" — it's data storytelling: choosing the
right chart for the right question, keeping every chart honest (zero-baseline axes,
no distortion), and stripping away anything that doesn't help the reader understand
the data faster.

## Files in This Repo
| File | Description |
|------|-------------|
| `Project4_DataVisualization_AyeshaSarwar.ipynb` | Main Jupyter notebook — all analysis and charts |
| `Dataset for Data Analytics - Sheet1.csv` | Source dataset (1,200 e-commerce orders) |
| `README.md` | This file |

## Dataset
- **Rows:** 1,200 orders
- **Date range:** January 2023 – June 2025
- **Columns:** OrderID, Date, CustomerID, Product, Quantity, UnitPrice,
  ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber, ItemsInCart,
  CouponCode, ReferralSource, TotalPrice

## What's Inside the Notebook
1. **Setup** — imports and a consistent, presentation-clean chart style
2. **Load the Data** — reads the CSV and parses dates
3. **Quick Exploratory Pass** — shape, dtypes, nulls, category counts (analyst-only view)
4. **The Architect** — a table defining the business question, analytical need, and
   chosen chart type *before* any chart is built
5. **Chart 1 — Bar:** revenue by product category
6. **Chart 2 — Line:** monthly revenue trend with a fitted trend line
7. **Chart 3 — Scatter:** relationship between quantity ordered and order value
8. **Chart 4 — Stacked Bar:** order status composition (Delivered/Shipped/Pending/
   Returned/Cancelled) by product
9. **The Editor** — a side-by-side distorted-vs-honest axis demo, explaining why every
   bar chart in this notebook starts at zero
10. **The Storyteller** — one final polished executive summary slide with an
    action-oriented recommendation
11. **Key Insights Summary** and a checklist mapping the notebook back to the brief's
    requirements

## Key Findings
- **Chairs** are the top revenue-generating product (~$195.6k), narrowly ahead of
  Printers; **Phones** generate the least (~$151.7k).
- **Revenue is trending slightly downward** over the 2.5-year window — a signal worth
  monitoring, not yet a crisis.
- **Order value scales with quantity purchased** (r ≈ 0.6) more strongly than with
  items placed in the cart (r ≈ 0.4).
- **~41% of all orders end in cancellation or return**, consistently across every
  product — a company-wide fulfillment issue. **Monitors** have the highest rate and
  are the recommended starting point for root-cause investigation.

## Design Principles Applied
- Zero-baseline axes on every bar chart (no truncation / "Lie Factor")
- No pie charts
- High data-ink ratio — no gridlines, no borders, no 3D effects
- One accent color per chart to highlight the answer to the question being asked
- Action-oriented chart titles that state the insight, not just the metric
- One insight per chart/slide

## How to Run
1. Make sure the dataset CSV is in the **same folder** as the notebook.
2. Install dependencies:
```bash
   pip install pandas numpy matplotlib
```
3. Open the notebook in Jupyter:
```bash
   jupyter notebook Project4_DataVisualization_AyeshaSarwar.ipynb
```
4. Run all cells in order (Cell → Run All), or step through with **Shift + Enter**.

## Author
Ayesha Sarwar — DecodeLabs Data Analytics Training, Batch 2026
