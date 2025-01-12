# Stochastic Stock Optimization Model

## Project Overview

This project showcases a stochastic stock optimization model designed to maximize portfolio returns while minimizing risk. 
The model leverages Mixed Integer Programming (MIP) to allocate investment capital across a portfolio of assets under varying market scenarios. 
The ultimate goal is to create a balanced, diversified portfolio that adheres to user-defined constraints and preferences for risk tolerance, diversification, and hedging effectiveness.
The project was created as part of a larger optimization exercise to simulate real-world decision-making under uncertainty, producing results that are interpretable for stakeholders such as financial advisors, portfolio managers, and analytics professionals.

The primary goals of this project include:

- **Practical Application:** To apply MIP in an area of interest and deliver a solution useful for a hypothetical client or user.
- **Collaboration with GenAI:** To utilize Generative AI for brainstorming and prototyping the optimization model.
- **Project Execution:** To execute a complete optimization project, from scoping the problem to presenting findings.
- 
---

## Key Objectives

1. **Maximize Annual Returns:** Allocates investment to maximize the annualized return of the portfolio.
2. **Minimize Risk:** Incorporates mean absolute deviation as a risk measure to stabilize portfolio performance.
3. **Handle Scenarios:** Adjusts portfolio allocations based on external market conditions (e.g., recessions, interest rate changes).
4. **Support Decision-Making:** Provides interpretable outputs to guide investment decisions while adhering to practical constraints.
5. 
---

## Key Features of the Model

### 1. **Objective Function**
The objective of the model is to maximize the expected return of the portfolio while minimizing its risk, represented as variance or another risk metric. 
The weighted return of selected stocks is balanced against the risk factor to achieve the optimal trade-off.

### 2. **Decision Variables**
- **Stock Inclusion:** Binary variables to indicate whether a stock is included in the portfolio.
- **Investment Proportion:** Continuous variables to represent the fraction of the total investment allocated to each stock.

### 3. **Constraints**
The model includes the following constraints:
- **Budget Constraint:** Ensures total investment equals 100% of available capital.
- **Risk Tolerance:** Guarantees a minimum expected return to maintain performance.
- **Diversification:** Limits maximum allocation to any single asset (e.g., 40%).
- **Hedging Effectiveness:** Enforces a minimum allocation to assets included in the portfolio.

---

## Scenario Analysis

The model incorporates **10 predefined market scenarios** that simulate realistic macroeconomic conditions:
- Recession
- Market Crash
- Economic Slowdown
- High/Low Interest Rates
- Inflation/Deflation
- Regulatory Changes
- Risk-Averse vs. Risk-Seeking Behaviors
Each scenario adjusts parameters like market drop, interest rates, and inflation to produce tailored portfolio allocations. For example:
- Recession: Reduces expected returns and increases diversification to mitigate risk.
- Risk-Seeking: Prioritizes high-return assets even under increased volatility.

---

## Methodology

**1. Data Preparation**
- Input: Historical asset return data
- Compute:
   - Mean returns
   - Mean absolute deviations
   - Annualized returns (assuming 252 trading days/year)
**2. Model Setup**
- Define the MIP model using the Pyomo library.
- Initialize parameters for risk and return.
**3. Scenario Application**
- Update parameters dynamically based on the selected scenario.
- Adjust weights for risk versus return in the objective function.
**4. Optimization**
- Solve the model using CBC solver.
- Output optimal asset allocations for the given budget and constraints.

---

## Results and Insights
The model generates:
**1. Optimal Portfolio Allocation:** Shows the proportion of capital to allocate to each asset.
**2. Scenario Comparisons:** Highlights how allocations change under different market conditions.
**3. Performance Trade-offs:** Balances between risk minimization and return maximization.

---

## Presentation Deliverables

### 1. **PowerPoint Slides**
- A standalone slide deck summarizing the project for an executive audience.
- Clear explanations of the model’s purpose, methodology, and outcomes.

### 2. **Model Code and Documentation**
- Fully documented Python code for the optimization model.
- Instructions for replicating the results with new datasets.

---

## Key Highlights

- **Performance Improvement:** Demonstrated superior results compared to benchmark models using equal-weighted portfolios.
- **Risk Analysis:** Incorporated scenario analysis to evaluate portfolio performance under varying market conditions.

---

## Future Extensions

- **Dynamic Optimization:** Extend the model to support dynamic rebalancing over multiple periods.
- **Integration with Machine Learning:** Use machine learning techniques to forecast stock returns and risks more accurately.
- **User Interface:** Develop a user-friendly interface for non-technical users.
- **Real-world Data Application:** Test the model with live financial data from APIs like Yahoo Finance or Bloomberg.

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Update_Final_Project_Code.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the optimization script:
   ```bash
   python optimize_portfolio.py
   ```

4. View results and visualizations in the `output/` folder.

---

# Requirements
Requirements
Python 3.8+
Pyomo: Optimization modeling language.
NumPy: For numerical computations.
Solver: CBC.

---

## Conclusion

This project demonstrates the power of optimization modeling in solving complex financial problems. By balancing returns and risks, the model offers a structured and efficient approach to portfolio management, making it a valuable tool for investors and financial analysts.

