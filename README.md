# Project-CalculoPrecios
Overview

This project demonstrates how to simulate and value a European option (Call or Put) using a combination of stochastic processes and quantitative finance models, including:

    The Black-Scholes partial differential equation
    Markov Chains for state-based price transitions
    ARCH (Autoregressive Conditional Heteroskedasticity) to capture time-dependent volatility
    Monte Carlo simulations for generating multiple price trajectories

By integrating these techniques, we obtain a more robust view of the underlying asset’s behavior—in this case, PepsiCo (PEP)—and calculate a fair price for the associated European options.
Key Highlights

    Data Collection from Yahoo! Finance
        Automatically retrieves one year of historical price data for PEP.
        Uses Python’s yfinance library to download and preprocess daily closing prices.
        Calculates logarithmic returns to capture relative price changes over time.

    Stochastic Models
        Black-Scholes Equation: Implements the classic analytical formula to estimate the fair value of a European Call/Put option.
        Markov Chain Approach: Models price transitions between discrete states; transition probabilities depend on the current state of the asset, not its entire history.
        ARCH Model: Captures time-dependent volatility, allowing more accurate modeling of financial returns than constant-volatility assumptions.

    Monte Carlo Simulation
        Generates multiple random price paths of PEP by sampling from the fitted distributions.
        Estimates the expected payoff of the option under each simulated path, discounting at a risk-free rate.
        Quantifies risk and uncertainty via the distribution of payoffs across simulations.

    Option Valuation
        Call/Put Pricing: Calculates theoretical option prices, depending on model parameters (volatility, time-to-maturity, strike price, and more).
        Sensitivity Analysis: Explores how changes in volatility, interest rates, or time to maturity affect option value.

    Results & Interpretations
        Comparison of Black-Scholes closed-form solutions vs. Monte Carlo simulations.
        Impact of modeling volatility with ARCH on option pricing.
        Practical insights for traders or investors evaluating PEP’s derivatives in a more realistic, volatility-aware framework.

Skills & Tools Demonstrated

    Python for Quantitative Finance
        Libraries: pandas, numpy, yfinance, statsmodels (for ARCH), matplotlib (for plotting and results visualization)
        Notebook: Jupyter/Colab environment for interactive exploration and clear presentation of results

    Statistical & Mathematical Modeling
        Moving Average / Standard Deviation calculations for baseline volatility
        ARCH for time-varying volatility modeling
        Markov Chains and state transition matrices

    Financial Engineering
        Pricing Formulas: Black-Scholes PDE, implied volatility considerations
        Risk-Neutral Valuation: Discounting expected payoffs using a risk-free rate
        Scenario Analysis: Monte Carlo approach to account for market fluctuations

    Data Cleaning & Preprocessing
        Handling NaN values, merging multiple datasets, adjusting for splits/dividends if necessary
        Log-return calculations to reduce bias and stabilize variance

    Presentation & Communication
        Clear explanation of methodology and interpretation of results
        Visual dashboards and plots to compare empirical vs. theoretical results
