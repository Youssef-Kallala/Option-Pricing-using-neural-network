# Computational Methods for Financial Options Pricing

This repository contains a Jupyter Notebook (`Code.ipynb`) that explores and implements various computational methods for pricing financial options. It covers both European and American options, moving from classical numerical models to Monte Carlo simulations and finally to a modern machine learning approach using a neural network.

## Overview

The notebook serves as an educational and practical guide to options pricing. It begins with the theoretical underpinnings of the Black-Scholes model and progressively implements four different pricing techniques, complete with explanations and visualizations.

### Methods Implemented

The following pricing models are demonstrated in the notebook:

1.  **Binomial Options Pricing Model:** A classic lattice-based method for pricing European options by modeling the underlying asset's price movement over discrete time intervals.
2.  **American Options Binomial Model:** An extension of the binomial model that accounts for the early-exercise feature of American options.
3.  **Longstaff-Schwartz Monte Carlo Method:** A sophisticated simulation technique for pricing American options. It uses backward induction and regression on Laguerre polynomials to estimate the option's continuation value at each time step.
4.  **Neural Network Price Approximation:** A deep learning model trained to learn and approximate the Black-Scholes formula for European call options, demonstrating the power of AI in replicating complex financial mathematics.

### Visualizations

The notebook includes several plots to help visualize the results and concepts, such as:
- Simulation of asset price paths using Geometric Brownian Motion.
- Convergence of the American option price as the number of binomial steps increases.
- A comparison of the continuation value vs. the immediate exercise value in the Longstaff-Schwartz method.
- Convergence of the Monte Carlo price as the number of simulation paths increases.

## Requirements

To run this notebook, you will need Python 3.x and the following libraries:

*   NumPy
*   Matplotlib
*   Scikit-learn
*   SciPy
*   PyTorch

You can install the dependencies using pip:
```bash
pip install numpy matplotlib scikit-learn scipy torch
```
**Note:** The original notebook execution shows a `ModuleNotFoundError` for `torch`. Please ensure you have it installed before running the final sections.

## How to Use

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name
    ```
2.  **Install the dependencies** as listed in the Requirements section.
3.  **Launch Jupyter Notebook or Jupyter Lab:**
    ```bash
    jupyter notebook
    ```
4.  Open `Code.ipynb` and run the cells sequentially to see the implementation and results of each pricing method.

## Notebook Structure

The notebook is divided into the following main sections:

1.  **Introduction to Options:** A theoretical overview of European and American options, including the Black-Scholes equation and formula.
2.  **Binomial Pricing Models:** Implementation of binomial models for both European and American options.
3.  **Longstaff-Schwartz Monte Carlo Method:** A detailed implementation for pricing American options with early exercise.
4.  **Neural Network for Pricing:** A demonstration of how a neural network can be trained to learn the Black-Scholes pricing function from synthetic data.

## Key Findings

- The notebook effectively demonstrates the price convergence of numerical methods like the binomial and Monte Carlo models as the number of steps or paths increases.
- The neural network successfully approximates the Black-Scholes formula with high accuracy, showcasing a powerful alternative for pricing complex derivatives.
