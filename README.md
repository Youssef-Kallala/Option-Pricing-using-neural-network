# Option Pricing Models

This repository contains a Jupyter Notebook that explores various methods for pricing financial options. It provides both theoretical explanations and practical implementations of popular option pricing models, ranging from the foundational Black-Scholes formula to modern neural network approaches.

## Features

*   **Black-Scholes Model**: Includes the foundational Black-Scholes equation and the formula for pricing European call options.
*   **Binomial Option Pricing Model**: Implements the binomial method for valuing American options, with visualizations of option values over time.
*   **Longstaff-Schwartz Monte Carlo Method**: A detailed implementation of this advanced method for pricing American options using backward induction and Laguerre polynomials.
*   **Neural Network for Option Pricing**: Demonstrates how a neural network can be trained to approximate the Black-Scholes model.
*   **Visualizations**: The notebook includes various plots to help visualize option prices, model convergence, and the behavior of different pricing methods.

## Getting Started

### Prerequisites

To run this notebook, you will need to have Python 3 and the following libraries installed:

*   matplotlib
*   numpy
*   torch
*   scikit-learn
*   scipy

### Installation

1.  Clone this repository to your local machine:
    ```bash
    git clone https://github.com/Youssef-Kallala/Option-Pricing-using-neural-network.git
    ```
2.  Navigate to the project directory:
    ```bash
    cd Option-Pricing-using-neural-network
    ```
3.  Install the required libraries using pip:
    ```bash
    pip install matplotlib numpy torch scikit-learn scipy
    ```

## Usage

1.  Open the `OptionPricing.ipynb` file in a Jupyter Notebook environment.
2.  Run the cells in the notebook to see the implementation and visualizations of the different option pricing models.
3.  You can modify the parameters in the code cells to explore how they affect the option prices.

## Models and Mathematical Concepts Explained

This notebook covers several key models for pricing financial options. Below is a conceptual overview of each.

### 1. The Black-Scholes Model

The Black-Scholes model is a cornerstone of financial mathematics for pricing European-style options.

*   **The Black-Scholes Equation** is a partial differential equation that describes how the price of an option evolves over time. It assumes a lognormal distribution of stock prices and considers factors like the underlying asset's price, volatility, time to expiration, and the risk-free interest rate.

*   **The Black-Scholes Formula** is the closed-form solution to the equation for a European call option. Conceptually, it calculates the option price as the difference between two parts:

    **$$
    C = S \, N(d_1) - K e^{-rT} N(d_2)
    $$ **

    *   **$S \, N(d_1)$**: Represents the expected benefit of receiving the stock if the option finishes in the money.  
    *   **$K e^{-rT} N(d_2)$**: Represents the present value of paying the strike price ($K$) if the option is exercised.
    
    In simple terms, it's what you expect to get minus what you expect to pay, with both values adjusted for probability and the time value of money.

### 2. Binomial Option Pricing

This method is particularly useful for pricing **American options**, which can be exercised at any time before expiration.

It works by breaking down the time to expiration into a series of discrete steps. At each step, the model assumes the stock price can only move to one of two possible values: one up and one down. This creates a "binomial tree" of all possible future stock prices.

The option's value is then calculated by working backward from the final nodes of the tree (at expiration) to the present. At each node, the model checks whether exercising the option early is more valuable than holding it, making it ideal for American options.

### 3. Longstaff-Schwartz Monte Carlo Method

This is a more advanced technique, also for pricing **American options**. It combines the flexibility of Monte Carlo simulation with a clever approach to handle the early-exercise feature.

1.  **Monte Carlo Simulation**: First, it simulates thousands of random potential paths for the underlying asset's price from the start date to the expiration date.
2.  **Backward Induction & Regression**: It then works backward in time from the expiration date. At each time step, it uses a **least-squares regression** (using Laguerre polynomials in this notebook) to estimate the "continuation value"—that is, the expected value of keeping the option alive rather than exercising it immediately.
3.  **Optimal Decision**: By comparing the immediate exercise value to the estimated continuation value at each step for every simulated path, the model determines the optimal exercise strategy and, ultimately, the option's price today.

### 4. Neural Network for Option Pricing

This section demonstrates a modern, data-driven approach. Instead of being programmed with a specific financial formula, a neural network is trained on a large dataset of option parameters (stock price, strike, time, etc.) and their corresponding Black-Scholes prices.

The network learns the complex, non-linear relationships between the inputs and the output price. After training, it can predict the price of a new, unseen option by acting as a highly effective function approximator, showcasing the power of AI in replicating complex financial mathematics.

## Contributing

Contributions are welcome! If you have any suggestions or improvements, please feel free to create a pull request or open an issue.
