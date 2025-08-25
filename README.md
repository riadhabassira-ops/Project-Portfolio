# ec216-wage-price-spiral
[README.md](https://github.com/user-attachments/files/21967201/README.md)
# Wage–Price Relationship — EC216 Group Empirical Project (2022–2023)

**Course:** EC216 Intermediate Macroeconomics & Data Analysis  
**Type:** University group empirical project  
**Topic:** Wage–Price Spiral — relationship between hourly wage (X) and price level (Y)  

## TL;DR
- Built a simple linear regression to quantify the wage–price relationship.
- Estimated model: `Price Level = -7.5763 + 37.9982 × Hourly Wage`.
- Fit quality: Adjusted R² ≈ 0.9938.

## Background
The project examines the **wage–price spiral** mechanism: when wages rise—often alongside low unemployment and stronger bargaining power—firms' costs increase and prices follow, potentially reinforcing further wage increases.

## Data
- Variables: **Hourly Wage** (independent), **Price Level** (dependent).
- Descriptives and histograms prepared per coursework brief.
- Note: For portfolio reproducibility, include **sample/synthetic** data here or link to the original dataset if publicly accessible and licensed.

## Method
- Linear regression (OLS) in R/RStudio as prescribed by the module.
- Model form: `Y = β₀ + β₁ X` where Y = price level, X = hourly wage.
- Key estimates (rounded):
  - Intercept (β₀): **-7.5763**
  - Slope (β₁): **37.9982**
  - Adjusted R²: **0.9938**

## Results
- Positive and sizable slope → higher hourly wages are associated with higher price levels.
- Very high Adjusted R² indicates the model explains most of the variation in the provided sample.
- **Caveat:** Intercept is not economically meaningful at wage = 0 and should not be over‑interpreted.

## Limitations & Next Steps
- Bivariate OLS omits key macro drivers (productivity, expectations, policy).
- Potential endogeneity (simultaneity) between wages and prices.
- Next steps:
  - Add control variables (e.g., unemployment, productivity, import prices).
  - Try time‑series diagnostics (stationarity, autocorrelation).
  - Explore a Phillips‑curve style specification or VAR for dynamics.

## Reproducibility
- Environment: R/RStudio.
- Suggested files for this repo:
  - `data/` (sample CSV or instructions to access original data)
  - `analysis.Rmd` or `notebooks/` with the regression code
  - `figures/` for histograms and fit plot
- Minimal R snippet:
  ```r
  df <- read.csv('data/sample.csv')
  model <- lm(price_level ~ hourly_wage, data = df)
  summary(model)
  ```

## Project Structure
```
.
├── README.md
├── data/              # sample or synthetic data (do NOT commit sensitive data)
├── notebooks/         # Rmd / R scripts
└── figures/           # exported charts
``

## Acknowledgements
EC216 module brief and group collaboration.
