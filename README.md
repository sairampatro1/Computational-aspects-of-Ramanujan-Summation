# Computational Aspects of Ramanujan Summation

This repository contains a Julia notebook demonstrating the computational aspects of Ramanujan summation using tail approximations. The notebook explores infinite series summation with Euler-Maclaurin (for non-alternating series) and Euler-Boole (for alternating series) methods, alongside computing Ramanujan constants for various series types. It is designed for academic purposes, particularly as part of a thesis.

## Features

- **Infinite Series Summation**:
  - Euler-Maclaurin tail approximations for non-alternating series.
  - Euler-Boole tail approximations for alternating series.
  - Error analysis via plots of `log10(|error|)` vs. number of correction terms (`m`).

- **Ramanujan Constants**:
  - Computation for general series (e.g., `x^n`), alternating series (e.g., `-exp(x)`), geometric series (e.g., `2^(-n)`), exponential series (e.g., `e^x`), and Euler-type series (e.g., with gamma functions).
  - Includes illustrative examples with numerical outputs.

- **High-Precision Computations**:
  - Uses `setprecision(256)` for accurate results.

## Requirements

- [Julia](https://julialang.org/downloads/) (version 1.6 or later)
- [Jupyter](https://jupyter.org/install) (for interactive notebook execution)

### Required Julia Packages
- `SymPy`
- `Plots`
- `Printf`
- `SpecialFunctions`
- `IJulia` (for Jupyter kernel)

## Installation

1. **Install Julia**: Download and install from the [official website](https://julialang.org/downloads/) (version 1.6+ recommended).
2. **Install Jupyter**: Follow instructions at [jupyter.org/install](https://jupyter.org/install).
3. **Install Julia Packages**: Open a Julia REPL and run:
   ```julia
   using Pkg
   Pkg.add("SymPy")
   Pkg.add("Plots")
   Pkg.add("Printf")
   Pkg.add("SpecialFunctions")
   Pkg.add("IJulia")
   ```
4. **Set Up Julia Kernel**: Ensure Jupyter recognizes Julia via `IJulia`.

## Usage

1. **Open the Notebook**: Launch Jupyter, navigate to this repository, and open `computational_aspects_ramanujan_summation.ipynb`.
2. **Run Cells**: Execute cells sequentially to compute sums and Ramanujan constants. Outputs include numerical results and error plots.
3. **View Plots**: Plots are saved in a `plots` folder in the repository directory.

## Code Structure

The notebook defines a module `Errorplot` with functions for:
- Computing Bernoulli numbers and Euler polynomials (cached).
- Tail approximations (Euler-Maclaurin and Euler-Boole).
- Series summation combining partial sums and tails.
- Error plotting against correction terms.
- Ramanujan constant calculations for diverse series types.

## Notes

- **Precision**: High-precision arithmetic (`setprecision(256)`) may slow execution but ensures accuracy.
- **Plotting**: Uses GR backend (`gr()`); ensure compatibility if issues arise.

## License

This project is for academic purposes as part of a thesis on Ramanujan summation computational aspects.