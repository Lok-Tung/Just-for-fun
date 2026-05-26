# Insurance Asset-Liability Management (ALM) Dashboard

## Business Problem
Insurance companies must ensure that future asset cash flows are sufficient to meet policyholder obligations while maintaining profitability and managing risk. Changes in interest rates significantly affect both asset values and liability valuations, creating potential balance sheet mismatches. 

This project demonstrates how ALM techniques can be applied to optimize asset allocation, reduce duration mismatch risk, and evaluate balance sheet resilience under different interest rate environments.

## Results Summary
The optimization framework successfully:
- Minimized cash flow mismatch between assets and liabilities.
- Improved duration alignment through duration-gap penalties.
- Maintained a positive surplus across various interest rate scenarios.
- Generated an interactive dashboard for real-time monitoring of ALM risk metrics.

### Key Metrics
| Metric | Value |
| :--- | :--- |
| **Asset PV** | 944.42 |
| **Liability PV** | 298.67 |
| **Surplus** | 645.75 |
| **Asset Duration** | 2.01Y |
| **Liability Duration** | 2.03Y |
| **Duration Gap** | -0.02Y |
| **ALM Status** | Well Matched |

## Financial Concepts Applied
This project incorporates advanced concepts utilized by insurance and institutional risk management teams:
- **Asset-Liability Management (ALM)**: Integrated balance sheet management.
- **Fixed Income Analytics**: Present Value (PV) and yield curve applications.
- **Duration Analysis**: Sensitivity assessment via Modified Duration.
- **Duration Gap Management**: Strategic risk immunization.
- **Cash Flow Matching**: Ensuring liquidity for policyholder obligations.
- **Scenario Analysis**: Stress testing portfolio resilience (bps shifts).
- **Portfolio Optimization**: Constrained numerical optimization for asset allocation.

## Future Enhancements
To evolve this project toward enterprise-grade LDI (Liability-Driven Investment) standards, future extensions include:
- **Convexity analysis** for higher-order risk measurement.
- **Stochastic interest rate simulations** (e.g., Hull-White or Vasicek models).
- **Interest rate swap hedging** to manage long-term duration exposure.
- **Dynamic portfolio rebalancing** based on rolling market data.
- **Monte Carlo scenario generation** for Value-at-Risk (VaR) analysis.

## Tech Stack
* **Python**: Core logic and numerical simulation.
* **NumPy / Pandas**: Financial data modeling.
* **SciPy (`optimize`)**: Solving for optimal asset weights.
* **Plotly**: Interactive visualization and reporting.

## Getting Started
### Execution
```bash
python alm_dashboard.py

