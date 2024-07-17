# Pathwise Valuation of Bond

This repository contains a Python implementation for the pathwise valuation of an option-free bond. The example used in this implementation demonstrates how to calculate the present value of a bond with varying interest rates over time.

## Overview

- **Bond Details**:
  - Par Value: $100
  - Maturity: 3 years
  - Coupon Rate: 5% (Annual payment)
  
- **Interest Rate Path**:
  - T = 0: 3.00%
  - T = 1: 5.20%
  - T = 2: 4.80%

## Files

- `pathwisevaluation.ipynb`: Jupyter Notebook containing the code for calculating the present value of the bond using a random pathwise method.

## Code Explanation

1. **Bond Definition**: The bond's details are initialized with its par value, maturity, and coupon rate.
2. **Path Definition**: The function `path_definer` generates random interest rate paths based on the defined nodes.
3. **Present Value Calculation**: The `pv_calculator` function computes the present value of the bond given a specific path, coupon payment, and par value.
4. **Execution**: The script calculates the present values for multiple paths and estimates the bond's value.

## Usage

To run the code, ensure you have the necessary libraries installed:

```bash
pip install numpy
