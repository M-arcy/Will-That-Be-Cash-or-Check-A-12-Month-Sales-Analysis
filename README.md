# Will That Be Cash or Check? — 12-Month Amazon Sales Analysis

## Table of Contents

- [Description](#description)
- [Key Findings](#key-findings)
- [Dashboard](#dashboard)
- [Installation](#installation)
- [Usage](#usage)
- [Author](#author)

<hr style="border: none; height: 10px; background-color: #003057;" />

## Name

Twelve Months of Amazon Sales Data — Exploratory Data Analysis, Forecasting, and Interactive Dashboard

## Description

This project analyzes __185,950 sales transactions__ across twelve months of 2019 to uncover purchasing patterns, identify top-performing products, and produce a sales forecast — then presents those findings in interactive dashboards built in both __Tableau__ and __Power BI__.

The analysis was conducted in __Python__ using a Jupyter notebook for the exploratory data analysis (EDA) phase, followed by time series forecasting using __Prophet__ — chosen because the data showed non-stationary behavior that made ARIMA a poor fit. Results were then brought into Tableau and Power BI to make findings accessible to a non-technical business audience.

This project has these files:
- `EDA-of-Amazon-Sales-Data.ipynb` — main Jupyter notebook covering data cleaning, EDA, and forecasting
- `Sales-Analysis.py` — Python script version of the analysis
- `Data/` — folder containing the raw sales dataset
- `VizGraphs/` — exported chart images generated during analysis
- `PowerBI Dashboards/` — Power BI dashboard in PDF format
- `forecast_plot.png` — output from the Prophet time series forecast
- `README.md` — provides an overview of the project

[Back to Top](#table-of-contents)

## Key Findings

**Dataset:** 185,950 transactions, cleaned to remove 545 null values (0.29% of data), resulting in a complete 12-column dataset ready for analysis.

**Top products by volume sold:**
| Product | Units Sold |
|---|---|
| USB-C Charging Cable | 21,903 |
| Lightning Charging Cable | 21,658 |
| AAA Batteries 4-pack | 20,641 |
| AA Batteries 4-pack | 20,577 |

Low-cost accessories dominated volume. Premium products like iPhones (6,842 units) and MacBook Pro Laptops (4,724 units) sold in lower quantities but at significantly higher price points — an important distinction for inventory planning and margin strategy.

**Forecasting approach:**
- An initial ARIMA assessment found the sales data to be non-stationary (trends and seasonality present)
- __Prophet__ was selected instead, as it explicitly models trends, seasonality, and growth without requiring stationarity
- The forecast accounts for known sales spikes such as Black Friday (November 29, 2019)

**Geographic and temporal patterns:**
- Sales were analyzed by city, state, and hour of order placement to identify when and where purchasing was highest
- Findings support targeted marketing decisions aligned with regional demand and peak ordering times

[Back to Top](#table-of-contents)

## Dashboard

The interactive Tableau dashboard allows you to explore sales by product, city, and time period:

## __[View the Interactive Sales Dashboard on Tableau Public](https://public.tableau.com/app/profile/marcy2817/viz/SalesDashboard_16540941999000/Dashboard2)__

A Power BI version is also included in the `PowerBI Dashboards/` folder as a PDF for reference.

[Back to Top](#table-of-contents)

## Installation

Clone the repository:

```bash
git clone https://github.com/M-arcy/Will-That-Be-Cash-or-Check-A-12-Month-Sales-Analysis.git
cd Will-That-Be-Cash-or-Check-A-12-Month-Sales-Analysis
```

Create and activate a virtual environment (recommended):

```bash
python -m venv venv
# On Mac/Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install pandas numpy matplotlib seaborn prophet jupyter
```

[Back to Top](#table-of-contents)

## Usage

Open the main analysis notebook:

```bash
jupyter notebook EDA-of-Amazon-Sales-Data.ipynb
```

Run all cells in order to reproduce the data cleaning, exploratory analysis, and forecast. To explore the interactive visualizations, use the Tableau Public link above.

## Support

For questions, open an issue on the [GitHub repository](https://github.com/M-arcy/Will-That-Be-Cash-or-Check-A-12-Month-Sales-Analysis/issues) or reach out via [LinkedIn](https://www.linkedin.com/in/marcy-misner/).

## Author

Developed by __Marcy Misner__.

For more of my work: [GitHub](https://github.com/M-arcy) | [LinkedIn](https://www.linkedin.com/in/marcy-misner/)

## License

This project is licensed under the MIT License.

[Back to Top](#table-of-contents)
