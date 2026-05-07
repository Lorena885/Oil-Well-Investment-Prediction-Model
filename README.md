# Oil Well Investment Prediction Model

## Project Overview

This project uses machine learning and statistical risk analysis to identify the best region for opening 200 new oil wells. The goal is to maximize expected profit while keeping the risk of financial loss below the business threshold.

## Business Problem

The company needs to decide where to invest a $100M budget for new oil wells. Three regions are available, each with geological data and oil reserve estimates. The selected region must provide strong expected returns while minimizing downside risk.

## Dataset

The project uses three regional datasets:

- `geo_data_0.csv`
- `geo_data_1.csv`
- `geo_data_2.csv`

Each dataset contains 100,000 wells and the following columns:

- `id`: unique well identifier
- `f0`, `f1`, `f2`: geological features
- `product`: oil reserve volume in thousand barrels

## Methodology

1. Loaded and explored the three regional datasets.
2. Checked for missing values and duplicates.
3. Split each dataset into training and validation sets.
4. Trained a Linear Regression model for each region.
5. Evaluated model performance using RMSE.
6. Selected the top 200 wells based on predicted reserves.
7. Estimated profit using actual reserve values.
8. Used bootstrap simulation to estimate average profit, confidence intervals, and risk of loss.

## Key Results

| Region | Average Profit | 95% Confidence Interval | Loss Risk |
|---|---:|---:|---:|
| Region 0 | $3.96M | -$1.11M to $9.10M | 6.90% |
| Region 1 | $4.61M | $0.78M to $8.63M | 0.70% |
| Region 2 | $3.93M | -$1.12M to $9.35M | 6.50% |

## Recommendation

Region 1 is the recommended investment location. It has the highest expected average profit and the lowest risk of loss, meeting the business requirement of keeping loss risk below 2.5%.

## Interactive Dashboard

An interactive dashboard was created to summarize the investment recommendation, model metrics, expected profit, and risk comparison by region.

To view it locally, open:

```text
dashboard/index.html
```

## Tools Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook
- Bootstrap simulation
- HTML, CSS, JavaScript
- Plotly

## Project Structure

```text
Oil-Well-Investment-Prediction-Model/
+-- datasets/
|   +-- geo_data_0.csv
|   +-- geo_data_1.csv
|   +-- geo_data_2.csv
+-- dashboard/
|   +-- index.html
|   +-- results.json
+-- Oil well investment prediction model notebook.ipynb
+-- README.md
```

## How to Run

1. Create and activate a virtual environment.
2. Install dependencies:

```bash
pip install pandas numpy scikit-learn ipykernel
```

3. Open the notebook in Jupyter Notebook or VS Code.
4. Run all cells.
5. Open `dashboard/index.html` to view the interactive dashboard.

## Final Outcome

The analysis recommends Region 1 as the optimal investment choice because it combines the highest expected average profit with the lowest estimated risk of loss.
