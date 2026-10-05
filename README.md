# Starbucks AB Testing and Experimentation

## Project overview

This project analyzes a randomized promotion experiment for a single product. The product generates $10 in revenue per purchase, and sending a promotion costs $0.15 per customer.

The analysis asks whether the promotion increases purchase rate, whether broad promotion covers its cost, and whether a customer-targeting strategy can improve the economics.

## Business questions

1. Does the promotion increase conversion rate?
2. Does broad promotion generate positive net incremental revenue (NIR)?
3. Can logistic regression identify customers whose estimated conversion-rate lift may cover the promotion cost?
4. Does the targeting strategy generate positive NIR when evaluated on separate randomized test data?

## Methods and tools

- Python: pandas, NumPy, Matplotlib, SciPy, statsmodels, scikit-learn
- A/B testing and experiment analysis
- Conversion rate comparison and two-proportion significance test
- Chi-square goodness-of-fit test for sample-ratio mismatch (SRM)
- Logistic regression for model-based treatment-effect estimation (uplift modeling)

## Key findings

- The promotion increased purchase rate in the overall experiment, but its average lift was below the 1.5 percentage-point break-even lift under the stated assumptions.
- The targeting rule selected 12,744 customers for evaluation.
- Among selected customers, purchase rate was 2.72% in treatment and 0.70% in control, a lift of 2.01 percentage points (approximate 95% CI: 1.56 to 2.46 percentage points).
- Estimated NIR was $0.05 per selected customer (approximate 95% CI: $0.006 to $0.096). The result meets the project’s agreed criteria for positive NIR.

## Limitations

The customer features are anonymized as `V1` through `V7`. The NIR calculation uses product revenue and promotion cost only; it excludes product and other business costs, so it is not profit. Customer features are anonymized, so their business meaning is unknown. 


