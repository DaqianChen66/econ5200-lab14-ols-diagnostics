# econ5200-lab14-ols-diagnostics
# OLS Diagnostics: Robust and Clustered Standard Errors

## Objective

I studied how heteroskedasticity, within-firm dependence, and influential observations affect OLS inference.

## Methodology

- Simulated heteroskedastic data and compared classical, HC1, and HC3 confidence intervals.
- Simulated a panel with 40 firms where employees shared firm-level shocks.
- Compared classical, HC3, and firm-clustered standard errors.
- Used leverage, studentised residuals, and Cook's distance to identify influential observations.
- Used AI to create a function that reports six types of standard errors and checked all results against statsmodels.

## Key Findings

With heteroskedastic errors, the nominal 95% interval covered the true slope 92.4% of the time with classical standard errors and 94.4% with HC3.

With errors shared within 40 firms, HC3 coverage was only 50.3%, while clustering by firm increased coverage to 93.7%. This showed that heteroskedasticity-robust standard errors do not correct within-group dependence.

The planted influential observations changed the estimated slope from 1.4927 to 1.4468. Cook's distance helped identify the observation that combined high leverage with a large residual.

I completed one AI round for the standard-error function. All 18 standard errors matched statsmodels exactly, and the renamed-column test also passed 18 of 18 checks.
