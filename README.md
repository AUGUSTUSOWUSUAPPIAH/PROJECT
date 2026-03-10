# Sports Betting Probability & Monte Carlo Simulation Analysis

## Overview

This project applies probability theory and Monte Carlo simulation to evaluate the profitability of a sports betting strategy in a best-of-three MLB series between the Boston Red Sox and the New York Yankees.

The betting structure is asymmetric:
- +$500 for each Red Sox win  
- -$520 for each Red Sox loss  

Using theoretical probability modeling and 10,000-trial simulation, this analysis evaluates whether scheduling affects expected profitability.

---

## Objectives

1. Compute the full theoretical probability distribution of net winnings  
2. Calculate expected value, variance, and standard deviation  
3. Construct a cumulative distribution function (CDF)  
4. Implement Monte Carlo simulation using inverse transform sampling  
5. Validate results with:
   - 95% confidence interval
   - Chi-squared goodness-of-fit test  
6. Conduct sensitivity analysis across win probability parameters  
7. Compare two scheduling configurations:
   - **BNB (Boston–New York–Boston)**
   - **NYN (New York–Boston–New York)**

---

## Methodology

### Theoretical Framework
- Modeled as a sequential Bernoulli process
- Game-level win probabilities:
  - Red Sox home win probability: 0.60
  - Yankees home win probability: 0.57
  - Red Sox away win probability: 0.43
- Series outcomes enumerated and aggregated by payoff
- Expected value and variance computed analytically

### Monte Carlo Simulation
- 10,000 trials
- Inverse transform sampling via Excel
- XLOOKUP used to map uniform random draws to payoff outcomes
- Running average convergence evaluated

### Statistical Validation
- 95% confidence interval for expected value
- Chi-squared goodness-of-fit test (df = 3)

---

## Key Results

### Boston–New York–Boston (BNB)

- Theoretical Expected Value: **+$57.89**
- Standard Deviation: ~$795
- 95% CI: [$44.45, $75.58]
- Chi-squared p-value: 0.734
- Strategy Verdict: **Profitable**

### New York–Boston–New York (NYN)

- Theoretical Expected Value: **-$31.24**
- Standard Deviation: ~$800
- Chi-squared p-value: 0.873
- Strategy Verdict: **Unprofitable**

---

## Strategic Insight

The difference in expected value (~$89 per series) is driven entirely by scheduling.

BNB provides:
- Two home games at 60% win probability
- One away game at 43%

NYN reverses this advantage.

Over 1,000 series:
- BNB → Expected gain ≈ $57,890  
- NYN → Expected loss ≈ $31,240  

Scheduling structure alone determines long-run profitability.

---

## Sensitivity Analysis

Profitability under BNB remains positive as long as:

Red Sox home win probability > ~0.54  
(assuming Yankees home win probability = 0.57)

This indicates robustness of the BNB strategy under moderate parameter variation.

---

## Tools Used

- Microsoft Excel
- Monte Carlo simulation
- Inverse Transform Sampling
- Probability modeling
- Chi-squared hypothesis testing

---

## Skills Demonstrated

- Probability distribution modeling
- Expected value & variance computation
- Monte Carlo simulation design
- Statistical validation
- Sensitivity analysis
- Decision strategy comparison

---

## Author

Augustus Kwame Owusu-Appiah  
MS Analytics 
Northeastern University

---

## Academic Context

Graduate-level probability and simulation analysis project.
