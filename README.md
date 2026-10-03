# Starbucks AB Testing and Experimentation

## Project overview

This project analyzes a randomized promotion experiment for a single product. The product generates $10 in revenue per purchase, and sending a promotion costs $0.15 per customer.

The analysis asks whether the promotion increases purchase rate, whether broad promotion covers its cost, and whether a customer-targeting strategy can improve the economics.

## Questions

1. Does the promotion increase purchase rate?
2. Does broad promotion generate positive net incremental revenue?
3. Can customer features help identify customers who may respond profitably to the promotion?
4. Does the targeting strategy show positive incremental value when evaluated on separate randomized test data?

## Methods and tools

- Python: pandas, NumPy, Matplotlib, SciPy, statsmodels, scikit-learn
- A/B testing and experiment analysis
- Purchase-rate comparison and two-proportion significance test
- Chi-square goodness-of-fit test for sample-ratio mismatch (SRM)
- Logistic regression

## Key findings

- The promotion increased purchase rate in the overall training experiment, but its estimated average lift did not cover the promotion cost under the stated assumptions.
- The targeting rule selected 12,232 customers for evaluation.
- Among selected customers, purchase rate was 2.60% in treatment and 0.65% in control, a lift of 1.96 percentage points (approximate 95% CI: 1.51 to 2.40 percentage points).
- Estimated net incremental revenue was $0.05 per selected customer (approximate 95% CI: $0.001 to $0.090), or about $557 across the selected group.
- The selected-group result met the project’s decision criteria for positive net incremental revenue.

## Business assumptions and limitations

The analysis treats $10 as product revenue per purchase and subtracts the $0.15 promotion cost. It does not include product, fulfillment, or other business costs, so net incremental revenue here is not the same as profit.

The customer features are anonymized as `V1` through `V7`. The model-based customer-level uplift estimates are uncertain; the targeting strategy is evaluated using randomized outcomes in the separate test data.

## Files

- `Starbucks AB Testing and Experimentation.ipynb` — analysis and results

