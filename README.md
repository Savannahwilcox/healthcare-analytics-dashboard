# Hospital-Acquired Infection (HAI) State Benchmarking

Analysis of CDC National Healthcare Safety Network (NHSN) 2023 Standardized Infection Ratios (SIR), benchmarking all 50 states, D.C., and Puerto Rico across seven infection types.

## Data source

CDC NHSN HAI Progress Report, "State SIR Comparison" tables (Tables 10a-10g): CLABSI, CAUTI, VAE, SSI following colon surgery, SSI following hysterectomy, MRSA, and CDI. SIR is risk-adjusted: 1.0 means a state matched the national baseline, above 1.0 is worse than expected, below 1.0 is better.

## Key findings

Connecticut has the best overall score (0.62 average across all seven infection types), followed by Wyoming (0.66), D.C. (0.66), and Delaware (0.67). Puerto Rico (1.17) and North Dakota (1.04) rank worst, with low scores across multiple infection types rather than one bad metric.

VAE (ventilator-associated events) is the hardest infection to prevent nationally, averaging 1.20, the only infection type where the national average is above the expected baseline. SSI following hysterectomy is second hardest (1.10 average). CDI is the best-controlled infection nationally, averaging 0.45.

The Northeast has the best regional average (0.78). The West has the worst (0.83). The South and Midwest are both slightly better than the national average.

## Methodology notes

D.C. appeared under two different spellings across CDC's tables ("D.C." in the CLABSI sheet, "D. C." in the SSI-colon-surgery sheet). Merging seven tables on `State` without normalizing this created two separate D.C. rows, each with only a partial set of infection scores. I normalized the spelling before merging so D.C.'s scores combine into one row (6 of 7 infection types reported; D.C. is one of the states that didn't report VAE that year).

"All US" is a national aggregate row in the raw CDC export, not a state or territory. Left in, it changes state-level rankings and gets grouped into "Other" along with D.C. and Puerto Rico, which lowers that region's average. I excluded it from every state-level and regional calculation.

## Live Dashboard

[The State of Hospital Infection Prevention in America](https://public.tableau.com/app/profile/savannah.wilcox4290/viz/TheStateofHospitalInfectionPreventioninAmerica/Dashboard1) — US map by region, comparison across all 7 infection types, and top/bottom 10 state rankings.

## Limitations

- SIR is risk-adjusted for patient mix, but only for the factors CDC's model accounts for.
- Not every state reports every infection type. Overall scores are averaged across whichever metrics a state reported.
- 2023 is the most recent year with full state-level SIR comparisons published. This is a single-year snapshot, not a trend.

## Tools

Python, pandas, Jupyter · Tableau Public

## Repository Structure

```text
├── data/
│   └── raw/              # Original CDC NHSN export
├── notebooks/
│   └── 01_data_exploration.ipynb
├── requirements.txt
└── README.md
```
