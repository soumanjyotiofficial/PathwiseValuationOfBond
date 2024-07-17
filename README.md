# PathwiseValuationOfBond
## Bond Valuation Script

This repository contains a Python script for valuing an option-free bond using different interest rate paths. The script generates possible interest rate paths and calculates the present value of the bond based on those paths. It also includes a specific case path for demonstration.

## Bond Details

- **Par Value**: $100
- **Maturity**: 3 years
- **Coupon Rate**: 5% (Annual payment)
- **Type**: Option-free

## Interest Rate Paths

- **Path 1**: 3.00% → 5.20% → 4.80%
- **Path 2**: Other randomly generated paths based on given nodes

## Script Details

The script performs the following steps:
1. **Defines interest rate nodes**:
    - T = 0: 3%
    - T = 1: 5.2%, 3.6%
    - T = 2: 6.3%, 4.8%, 4%

2. **Generates random interest rate paths**:
    - Uses the `path_definer` function to generate unique paths from the nodes.
    
3. **Calculates the present value of the bond for each path**:
    - Uses the `pv_calculator` function to compute the present value of the bond given a path, coupon payment, and par value.

4. **Estimates the value of the bond**:
    - Calculates the mean present value across all generated paths.

## How to Use

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/bond-valuation.git
    cd bond-valuation
    ```

2. **Install dependencies**:
    The script requires `numpy`. Install it using pip:
    ```sh
    pip install numpy
    ```

3. **Run the script**:
    ```sh
    python bond_valuation.py
    ```

## Functions

- **path_definer(trial, nodes)**: Generates unique interest rate paths.
  - `trial`: Number of unique paths to generate.
  - `nodes`: List of lists containing interest rate nodes.

- **pv_calculator(path, cpn, par)**: Calculates the present value of the bond given an interest rate path.
  - `path`: List of interest rates.
  - `cpn`: Coupon payment.
  - `par`: Par value of the bond.

## Example Output

The script calculates the estimated value of the bond using both the generated paths and a specific case path [3, 5.2, 4.8].

### Estimated Value of Bond
