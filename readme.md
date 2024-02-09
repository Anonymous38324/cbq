# Conditional Bayesian Quadrature

This repository contains the implementation of the code for the paper "Conditional Bayesian Quadrature". In the code, the algorithm proposed in the paper is "CBQ", the baseline methods are Least-square Monte Carlo (LSMC), Kernelized least-square Monte Carlo estimator (KLSMC), and Importance Sampling (IS).

## Installation

To install the necessary requirements, use the following command:

`pip install -r requirements.txt`

## Reproducing Results

### Synthetic Experiment: Bayesian Sensitivity Analysis for Linear Models

To reproduce the results (Figure 2 (Left & Middle)), run the following command:

`python bayes_sensitivity.py --dim 2 --fn f3 --kernel_x rbf --kernel_theta matern`

You can vary the dimension by altering the argument 'dim --2' to reproduce Figure 2 (Right).

### Bayesian Sensitivity Analysis for the Susceptible-Infectious-Recovered (SIR) Model

To reproduce the results (Figure 4 (Left)), run:

`python SIR.py`

### Option Pricing in Mathematical Finance

To reproduce the results using Stein kernels (Figure 4 (Right)), run:

`python black_scholes.py --kernel_theta rbf --kernel_x stein_matern`

And to reproduce the results not using Stein kernels (Figure 4 (Right)), run:

`python black_scholes.py --kernel_theta rbf --kernel_x log_normal_rbf`


### Uncertainty Decision Making in Health Economics

To reproduce the results (Figure 5), run:

`python health_economics.py`
