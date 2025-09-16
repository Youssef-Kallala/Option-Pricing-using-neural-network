# Option Pricing Models

This repository contains a Jupyter Notebook that explores various methods for pricing American options. It provides both theoretical explanations and practical implementations of popular option pricing models.

## Features

*   **Black-Scholes Model**: Includes the foundational Black-Scholes equation and the formula for pricing European call options.
*   **Binomial Option Pricing Model**: Implements the binomial method for valuing American options, with visualizations of option values over time.
*   **Longstaff-Schwartz Monte Carlo Method**: A detailed implementation of this advanced method for pricing American options using backward induction and Laguerre polynomials.
*   **Neural Network for Option Pricing**: Demonstrates how a neural network can be trained to approximate the Black-Scholes model for European call options.
*   **Visualizations**: The notebook includes various plots to help visualize the option prices and the convergence of the Monte Carlo simulations.

## Table of Contents

*   [Getting Started](#getting-started)
    *   [Prerequisites](#prerequisites)
    *   [Installation](#installation)
*   [Usage](#usage)
*   [Mathematical Background](#mathematical-background)
*   [Contributing](#contributing)
*   [License](#license)

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
3.  Install the required libraries. You can do this using pip:
    ```bash
    pip install matplotlib numpy torch scikit-learn scipy
    ```

## Usage

1.  Open the `OptionPricing.ipynb` file in a Jupyter Notebook environment.
2.  Run the cells in the notebook to see the implementation and visualizations of the different option pricing models.
3.  You can modify the parameters in the code cells to explore how they affect the option prices.

## Mathematical Background

The notebook covers the following key formulas and concepts:

![Mathematical Formulas](mathematical_formulas.png)

## Contributing

Contributions are welcome! If you have any suggestions or improvements, please feel free to create a pull request or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
