# Monthly Operations Review — Branch Performance Analysis

## Project Overview

This project analyzes the monthly performance of three store branches using sales, operating cost, and customer feedback data. The goal is to calculate profitability, compare net profit visually, rank customer experience, and make a manager-level recommendation using both financial and qualitative evidence.

This folder is designed to be Tableau-ready. Import `data/branch_operations_raw.csv` or `data/branch_operations_analysis.csv` into Tableau Public/Desktop to recreate the dashboard.

---

## Files Included

```text
data/
  branch_operations_raw.csv
  branch_operations_analysis.csv
  branch_c_bonus_scenario.csv

visuals/
  net_profit_by_branch.png

docs/
  submission_response.md

tableau/
  tableau_build_guide.md
```

---

## Core Calculations

### Net Profit

```text
Net Profit = Total Sales - Operating Cost
```

### Profit Margin %

```text
Profit Margin % = Net Profit / Total Sales
```

---

## Results Summary

| Branch | Total Sales | Operating Cost | Net Profit | Profit Margin % | Customer Rank |
|---|---:|---:|---:|---:|---:|
| Branch A | $45,000 | $32,000 | $13,000 | 28.89% | 2 |
| Branch B | $38,500 | $21,000 | $17,500 | 45.45% | 1 |
| Branch C | $52,000 | $48,000 | $4,000 | 7.69% | 3 |

---

## Customer Experience Ranking

1. **Branch B** — Best customer experience because feedback mentions reliable stock availability and friendly staff.
2. **Branch A** — Positive service feedback, but long queues hurt the overall experience.
3. **Branch C** — Weakest customer experience because customers mention expensive shipping and slow delivery.

---

## Manager Recommendation

Branch B should receive the **Performance Bonus** because it has the highest net profit at **$17,500**, the strongest profit margin at **45.45%**, and the best customer feedback. Branch A is performing reasonably well financially, but long queues show there is room to improve the customer experience. Branch C needs a **Process Improvement** plan because it has the highest sales but very high operating costs, leaving only **$4,000** in profit and a weak **7.69%** margin. Its feedback also points to shipping and delivery issues, so cost control and fulfillment efficiency should be the priority.

---

## Bonus Challenge: Branch C Cost Reduction Scenario

If Branch C reduced operating costs by 15%:

```text
Original Operating Cost = $48,000
Cost Reduction = $48,000 x 15% = $7,200
New Operating Cost = $48,000 - $7,200 = $40,800

New Net Profit = $52,000 - $40,800 = $11,200
New Profit Margin = $11,200 / $52,000 = 21.54%
```

### Bonus Result

| Metric | Value |
|---|---:|
| New Operating Cost | $40,800 |
| New Net Profit | $11,200 |
| New Profit Margin % | 21.54% |

---

## Suggested Tableau Dashboard Layout

**Dashboard Title:** Monthly Operations Review — Branch Performance

Recommended layout:

- Top left: Net Profit by Branch bar chart
- Top right: Branch Performance Summary table
- Bottom left: Customer Experience Ranking
- Bottom right: Manager Recommendation and Bonus Challenge

---

## Tableau Calculated Fields

Create these calculated fields in Tableau if using the raw CSV.

### Net Profit

```tableau
[Total Sales] - [Operating Cost]
```

### Profit Margin %

```tableau
[Net Profit] / [Total Sales]
```

Format `Profit Margin %` as a percentage with two decimal places.
