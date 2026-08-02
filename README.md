# Healthcare-Associated Infections (HAI) Analysis Dashboard

**Status:** Complete

Analyzing CDC data on hospital-acquired infections to identify trends, benchmark performance, and highlight areas for improvement.

## Project Overview

This project examines national and state-level HAI data from the CDC to answer:
- Which infections are most prevalent?
- How have rates changed over time?
- Which states perform best/worst?
- What's the impact on patient safety?

## Data Source

CDC National Healthcare Safety Network (NHSN) - HAI Progress Reports
- Source: https://www.cdc.gov/healthcare-associated-infections/php/data/index.html
- Infection types: CLABSI, CAUTI, CDI, MRSA, SSI, VAE
- Coverage: U.S. acute care hospitals (national + state level)

## Interactive Dashboard

**View the live dashboard:** [The State of Hospital Infection Prevention in America](https://public.tableau.com/app/profile/savannah.wilcox4290/viz/TheStateofHospitalInfectionPreventioninAmerica/Dashboard1)

The Tableau Public dashboard includes:
- US state map showing infection prevention performance by region
- Comparison of 7 infection types (CLABSI, CAUTI, VAE, etc.)
- Top 10 worst-performing states
- Top 10 best-performing states

**Key Findings:**
- Connecticut leads with the best overall performance (0.62 score)
- VAE (Ventilator-Associated Events) is the biggest challenge nationwide (1.20 avg)
- Northeast performs best; West lags behind
- Puerto Rico and North Dakota struggle most

## Project Structure

```
├── data/
│   ├── raw/            # Original CDC data
│   └── processed/      # Cleaned data for analysis
├── notebooks/
│   └── 01_data_exploration.ipynb
├── src/
│   └── utils.py
├── dashboards/
│   └── README.md        # Tableau dashboard documentation
├── outputs/
│   └── visualizations/
├── requirements.txt
└── README.md
```

## Reproducing This Locally

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Then run the notebooks in `notebooks/` in order to reproduce the cleaning and exploration steps behind the dashboard.
