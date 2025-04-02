# Computational-aspects-of-Ramanujan-Summation
# Infinite Series Summation using Tail Approximations

This repository contains a Julia notebook that demonstrates the computation of infinite series sums using Euler-Maclaurin (for non-alternating series) and Euler-Boole (for alternating series) tail approximations. The notebook includes examples showcasing the summation of different infinite series, along with plots to analyze the error relative to the number of correction terms used in the approximation.

## Features

- Computes infinite series sums using tail approximations.
- Supports both non-alternating and alternating series.
- Provides error analysis through plots of `log10(|error|)` vs. the number of correction terms (`m`).
- Utilizes high-precision arithmetic for accurate results.

## Requirements

- [Julia](https://julialang.org/downloads/) (version 1.6 or later) - Must be installed to run the code.
- [Jupyter](https://jupyter.org/install) (for interactive notebook execution)

## Installation

1. **Install Julia**: Download and install Julia from the [official website](https://julialang.org/downloads/). Ensure you have version 1.6 or later.

2. **Install Required Packages**: Open a Julia REPL and run the following commands to install the necessary packages:
   ```julia
   using Pkg
   Pkg.add("SymPy")
   Pkg.add("Plots")
   Pkg.add("Printf")
   Pkg.add("SpecialFunctions")
   Pkg.add("IJulia")  # For Jupyter kernel
   ```

3. **Set Up Jupyter**: If you haven't already, install Jupyter. Then, ensure the Julia kernel is available by running `Pkg.add("IJulia")` as above.

## Usage

1. **Open the Notebook**: Launch Jupyter and open the provided notebook file (`infinite_series_summation.ipynb`).

2. **Run the Cells**: Execute the cells one by one to see the results for each example. Each example computes the sum of an infinite series using tail approximations and displays a plot of the error versus the number of correction terms.

3. **Interpret the Results**: The plots show how the approximation error decreases as more correction terms are included. The numerical outputs provide the approximated sum and the corresponding error for different values of `m`.

## Examples

The notebook includes examples such as:
- Summation of `(-1)^n / sqrt(n)` ≈ -0.60490 (alternating series).
- Summation of `1/n` (non-alternating, divergent series approximated with Euler-Maclaurin).
- Additional examples can be added by defining new series functions and calling the `run_example` function.

## Module Overview

The code is organized into a module named `Analytictail`, which contains functions for:
- Computing Bernoulli numbers and Euler polynomials with caching.
- Calculating tail approximations using Euler-Maclaurin and Euler-Boole methods.
- Summing the series with partial sums and tail corrections.
- Plotting the error versus the number of correction terms.

You can reuse or extend this module in your own projects by importing it and utilizing its functions.

## Notes

- The computations use high-precision arithmetic (`setprecision(256)`) to ensure accuracy, which may result in slower execution times.
- The plotting backend is set to GR (`gr()`). If you encounter issues, ensure that the GR backend is properly installed and configured.

## License

This project is licensed under the MIT License.

## Contact

For questions or issues, please open an issue on this repository or contact [Your Name] at [Your Email].