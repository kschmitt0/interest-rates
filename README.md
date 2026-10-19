# Interest Rates and Cap Rate Forecasting

An R/Quarto analysis that tests how well a vector autoregression (VAR) model forecasts commercial real estate cap rates from the 10-year Treasury yield and the federal funds rate.

## Approach
- **Data:** monthly observations, April 2013 to March 2024: cap rate, 10-year Treasury yield (DGS10), and federal funds rate (DFF). Cap rate source: [add source].
- **Preparation:** second-differenced DGS10 and DFF to make them stationary.
- **Model:** lag order chosen with `VARselect` (max 15); VAR(4) with a constant; 12-month forecasts with 95% intervals.
- **Evaluation:** a model fit on April 2013 to March 2023 was compared with actual values for April 2023 to March 2024 using line plots, absolute errors, and MAPE. The model was then re-estimated on the full sample.

## Tools
R: `vars`, `forecast`, `tseries`, `mFilter`, `TSstudio`, `tidyverse`, `readxl`

## Status
Complete.

## Reproducing
Render `InterestRates.qmd` in RStudio. The Excel data files are not included in this repository.
