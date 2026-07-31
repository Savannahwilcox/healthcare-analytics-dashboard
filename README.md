# Healthcare-Associated Infections (HAI) Analysis Dashboard

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

## Project Structure
├── data/
│ ├── raw/ # Original CDC data
│ └── processed/ # Cleaned data for analysis
├── notebooks/
│ └── 01_data_exploration.ipynb
├── src/
│ └── utils.py
├── dashboards/
│ └── README.md # Tableau dashboard documentation
├── outputs/
│ └── visualizations/
├── requirements.txt
└── README.md
## Next Steps

- [ ] Download CDC HAI data
- [ ] Exploratory data analysis
- [ ] Data cleaning & preparation
- [ ] Tableau dashboard development
- [ ] Final dashboard deployment

## Getting Started

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
