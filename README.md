# Monte Carlo Option Pricing

European option pricing via Monte Carlo simulation using Geometric 
Brownian Motion, with convergence analysis against the Black-Scholes 
analytical solution.

## Overview
This project simulates 100,000 stock price paths under risk-neutral 
measure to price European call and put options, validating results 
against Black-Scholes and analyzing convergence behavior across 
simulation sizes.

## Method
- Simulate terminal stock prices using Geometric Brownian Motion (GBM)
- Discount expected payoffs to present value under risk-neutral measure
- Benchmark against Black-Scholes closed-form solution

## Results
| Metric | Value |
|---|---|
| MC Call Price (100K sims) | $10.4739 |
| Black-Scholes Call Price | $10.4506 |
| Difference | $0.0233 |
| Convergence (10K sims) | $0.0004 error |

## Key Findings
MC converges to the Black-Scholes price at ~10,000 simulations 
(error < $0.001), demonstrating the Law of Large Numbers. Monte Carlo's 
advantage over closed-form solutions is flexibility — it naturally 
extends to path-dependent options (Asian, barrier) where no analytical 
solution exists.

## Visualizations
<img width="1390" height="1014" alt="image" src="https://github.com/user-attachments/assets/7ed891b4-b3bd-423e-8d58-d61e763d32d9" />

## Technologies
Python, NumPy, SciPy, Matplotlib

## Author
Krisha Silwal
