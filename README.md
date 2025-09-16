# MIE1622---Portfolio-Selection-Strategies-with-CPLEX

This project compares different portfolio rebalancing strategies using the classical Markowitz model, accounting for trading costs and practical constraints. The strategies were implemented in Python with IBM CPLEX.

## Problem Setup
- Dataset: Adjusted closing prices of 30 U.S. stocks (2020–2021, 2023–2024)
- Initial portfolio value: ~$1,000,000 USD  
- Constraints:  
  - No short selling (weights ≥ 0)  
  - Budget constraint (sum of weights = 1)  
  - Transaction costs = 0.5% of traded volume  
  - Cash account must remain nonnegative  

## Strategies Implemented
1. **Buy and Hold** – Hold initial portfolio for 2 years without rebalancing  
2. **Equally Weighted** – Invest equally across all 30 assets  
3. **Minimum Variance** – Minimize portfolio variance  
4. **Maximum Expected Return** – Maximize expected returns  
5. **Maximum Sharpe Ratio** – Optimize risk-adjusted returns  

Additional improvements tested:  
- **1/n Buy and Hold** (no rebalancing after initial allocation)  
- **Maximum Expected Return with Sector Constraints** (sector weights capped at 25%)  

## Results
- **Maximum Return**: Achieved highest portfolio value but suffered the largest variance and drawdowns (~45%)  
- **Minimum Variance**: Lowest volatility and smallest drawdowns, but limited upside  
- **Maximum Sharpe Ratio**: Balanced diversification and return, suitable for moderate risk profiles  
- **Equally Weighted**: Provided stability but not optimal return  
- **1/n Buy and Hold**: Robust, lower transaction costs, competitive Sharpe ratio  
- **Max Return with Sector Constraints**: Reduced drawdowns and improved Sharpe ratio compared to unconstrained version  

## Skills Demonstrated
- Mean-variance optimization and quadratic programming  
- Portfolio rebalancing under transaction costs  
- Implementation of trading strategies in Python with CPLEX  
- Risk analysis: variance, Sharpe ratio, maximum drawdown  
- Scenario testing across two market periods (2020–2021 vs 2023–2024)  

