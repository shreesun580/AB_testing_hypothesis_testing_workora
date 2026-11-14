# A/B Testing & Hypothesis Testing – Website Checkout Experiment

**Statistical Analysis | Python | Pandas | SciPy | Statsmodels | Data Visualization**

**Prepared by: S. SHREE VATHY**

---

## 1. Project Overview

This project evaluates the performance of two website checkout experiences using A/B testing and statistical hypothesis testing.

The objective is to determine whether the modified checkout experience (Variant B) produces a statistically significant improvement in conversion rate compared with the existing checkout experience (Control A).

A two-proportion Z-test was performed to evaluate the conversion difference, calculate the p-value, estimate the 95% confidence interval, and measure the effect size.

## 2. Business Objective

- Compare the conversion performance of Control A and Variant B.
- Measure the absolute and relative conversion lift.
- Test whether the observed difference is statistically significant.
- Estimate the sample size required for a future experiment.
- Recommend whether to retain the existing checkout or launch the modified experience.

## 3. Dataset Description

**Dataset:** `checkout_ab_test_v2.csv`

**Dataset Dimensions:** 1,200 rows × 8 columns

| Column | Description |
|---|---|
| VisitorID | Unique visitor identifier |
| Variant | Experiment group (A or B) |
| Timestamp | Visitor experiment timestamp |
| Device | Visitor device category |
| TrafficSource | Traffic acquisition source |
| CheckoutStarted | Whether checkout was started |
| Converted | Whether the visitor completed a conversion |
| OrderValueINR | Order value in INR |

### Data Quality Validation

- Total records: 1,200
- Unique visitors: 1,200
- Missing values: 0
- Duplicate records: 0
- Control A visitors: 600
- Variant B visitors: 600

No data cleaning was required for the validated dataset.

## 4. Tools & Technologies

- Python
- Jupyter Notebook
- Pandas and NumPy
- Matplotlib and Seaborn
- SciPy
- Statsmodels

## 5. Hypothesis Formulation

**Null Hypothesis (H₀):**

There is no statistically significant difference in conversion rates between Control A and Variant B.

**Alternative Hypothesis (H₁):**

There is a statistically significant difference in conversion rates between Control A and Variant B.

**Testing Configuration:**

- Statistical Test: Two-Proportion Z-Test
- Test Type: Two-tailed
- Significance Level (α): 0.05
- Confidence Level: 95%
- Statistical Power Target: 80%

## 6. Conversion Performance Analysis

| Metric | Control A | Variant B |
|---|---:|---:|
| Total Visitors | 600 | 600 |
| Conversions | 57 | 71 |
| Non-Conversions | 543 | 529 |
| Conversion Rate | 9.50% | 11.83% |

**Key Observation:**

Variant B recorded 71 conversions compared with 57 conversions for Control A.

- Absolute Conversion Lift: +2.33 percentage points
- Relative Conversion Lift: +24.56%

Variant B performed better numerically, but statistical testing is required before declaring it the winner.

## 7. Statistical Hypothesis Testing

| Statistical Metric | Result |
|---|---:|
| Z-Statistic | 1.3092 |
| P-Value | 0.1905 |
| Significance Level | 0.05 |
| 95% Confidence Interval | -1.18 to +5.85 percentage points |
| Cohen's h | 0.0757 |
| Effect Size | Small |

### Statistical Interpretation

The p-value (0.1905) is greater than the significance level (0.05).

The 95% confidence interval includes zero, indicating that the true conversion difference could be negative, zero, or positive.

Therefore, we fail to reject the null hypothesis.

**Conclusion:** The experiment does not provide sufficient statistical evidence that Variant B improves checkout conversion.

## 8. Effect Size Analysis

Cohen's h was used to measure the difference between the two conversion proportions.

- Cohen's h: 0.0757
- Effect Size Category: Small

Although Variant B showed a 24.56% relative conversion lift, the standardized effect size is small.

## 9. Sample Size & Statistical Power Analysis

The estimated sample size required to detect an effect of the observed magnitude with 80% power and a 5% significance level:

| Metric | Visitors |
|---|---:|
| Current Sample per Group | 600 |
| Required Sample per Group | 2,740 |
| Required Total Sample | 5,480 |

The current experiment may be underpowered to detect an effect of this size.

This estimate is based on the observed conversion rates and assumes that the observed effect is the effect worth detecting. Actual future conversion rates may differ.

## 10. Visualizations

### Conversion Rate Comparison

![Conversion Rate Comparison](ab_conversion_comparison.png)

### 95% Confidence Interval

![Confidence Interval Analysis](ab_confidence_interval.png)

The confidence interval crosses zero, visually supporting the conclusion that the observed conversion difference is not statistically significant.

## 11. Executive Business Recommendation

**Decision: Keep Control A for now.**

Although Variant B achieved a higher observed conversion rate, the difference is not statistically significant.

Recommended business actions:

1. Retain the existing Control A checkout experience.
2. Plan a larger follow-up experiment.
3. Define a minimum practically meaningful conversion improvement before testing.
4. Collect sufficient visitor data to improve statistical power.
5. Re-evaluate the results before considering a permanent rollout.

Launching Variant B as a proven winner based on the current experiment would be premature.

## 12. Project Deliverables

- Validated A/B testing dataset
- Jupyter Notebook containing the statistical analysis
- Conversion rate comparison chart
- 95% confidence interval visualization
- Statistical hypothesis testing results
- Sample size and power analysis
- Executive decision memo
- Final PDF statistical report

## 13. Dataset Limitations

- The dataset is synthetic and intended for analytical practice.
- The experiment contains 600 visitors per group.
- The observed conversion lift is not statistically significant.
- The sample-size estimate is based on the observed effect and may change with future data.
- The analysis does not establish that the checkout variation caused a real-world business improvement.

## 14. Final Conclusion

Variant B achieved a higher observed conversion rate than Control A. However, the p-value of 0.1905 and the 95% confidence interval indicate insufficient evidence of a statistically significant improvement.

The appropriate business decision is to retain Control A temporarily and conduct a larger follow-up experiment before making a permanent implementation decision.

---

**Project By: S. SHREE VATHY**

*Data Analytics | A/B Testing | Statistical Hypothesis Testing*
