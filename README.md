## Thermal Leptogenesis Boltzmann Solver

This project implements a numerical solver for the coupled Boltzmann equations describing thermal leptogenesis in the early Universe. 
The code evolves the abundance of a heavy right-handed neutrino 𝑁1 and the resulting 𝐵−𝐿 asymmetry as functions of the temperature variable

𝑧 = 𝑀1/𝑇

CP-violating decays of the heavy neutrino generate a lepton asymmetry which partially survives washout processes.
This surviving 𝐵−𝐿 asymmetry is converted into a baryon asymmetry through electroweak sphaleron processes, allowing comparison with the observed baryon asymmetry of the Universe.

## Physics Model

The code solves the standard one-flavor thermal leptogenesis Boltzmann equations

𝑑𝑌𝑁1/𝑑𝑧 = −𝐷(𝑧)(𝑌𝑁1/𝑌𝑒𝑞 - 1)

𝑑𝑌(𝐵−𝐿)/𝑑𝑧 = −𝜖1𝐷(𝑧)(𝑌𝑁1/𝑌𝑒𝑞 − 1) − 𝑊(𝑧)𝑌(𝐵−𝐿)

The baryon asymmetry is obtained from sphaleron conversion

Y𝐵 = 28/79 𝑌(𝐵−𝐿)

## Numerical Method

- To handle the stiffness of the Boltzmann system, the solver uses
- RK4 integration in the non-stiff regime
- Implicit backward Euler in the stiff regime
- Cross-validation with SciPy's BDF stiff solver

## Features

- Solver for thermal leptogenesis Boltzmann equations
- Calculation of decay and washout rates using modified Bessel functions
- Hybrid RK4 / implicit integration scheme
- SciPy BDF validation
- Computation of baryon asymmetry and comparison with the observed value
- Visualization of 𝑌𝑁1, 𝑌(𝐵−𝐿), and reaction rates

## Requirements

- numpy
- scipy
- matplotlib

Install with

```bash
pip install numpy scipy matplotlib
```

## Running the Code

Run the notebook and choose either default benchmark parameters or custom inputs to explore different leptogenesis scenarios.
The program computes the evolution of the heavy neutrino abundance and the 𝐵−𝐿 asymmetry, produces plots, and estimates the resulting baryon asymmetry.
