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


This project focuses on **valuing a European option** (Call or Put) using **stochastic modeling** and **quantitative finance** techniques. The underlying asset is **PepsiCo (PEP)**, and the simulation draws on:

1. **Data Retrieval**: Daily historical stock prices from Yahoo! Finance using Python’s `yfinance`, followed by preprocessing (log returns, handling missing values).

2. **Black-Scholes Equation**: Applies the classic formula for European option pricing, assuming constant volatility and a lognormal distribution of returns.

3. **Markov Chains**: Models price transitions as state-based probabilities, capturing how prices evolve from one discrete state to another based on the current state.

4. **ARCH Model**: Addresses **time-varying volatility**, recognizing that price fluctuations often show volatility clustering, a limitation in basic Black-Scholes assumptions.

5. **Monte Carlo Simulation**: Generates multiple possible future price paths for PEP, incorporating drift and volatility parameters. By discounting payoffs across these scenarios, the project estimates the **expected value** of the option at expiration.

Key deliverables include:
- **Comparisons** between the closed-form Black-Scholes result and the **simulated** Monte Carlo valuations.  
- **Analysis** of how **ARCH-derived volatility** can refine pricing by reflecting conditional heteroskedasticity.  
- **Visual dashboards** and plots to illustrate differences in option values under various assumptions.

Technically, this project highlights:
- **Python** libraries (`numpy`, `pandas`, `matplotlib`, `statsmodels`)  
- **Quantitative finance** methods (risk-neutral valuation, implied volatility concepts)  
- **Data pipeline** tasks (cleaning, feature engineering)  
- **Communication skills** in explaining results and guiding stakeholders.

By integrating **Black-Scholes, Markov Chain transitions, and ARCH volatility** within a **Monte Carlo** framework, the project offers a **comprehensive approach** to option pricing. It demonstrates how combining multiple models and simulations can yield **more accurate** estimations of option values, helping traders or financial analysts make **data-driven decisions** in uncertain markets.
