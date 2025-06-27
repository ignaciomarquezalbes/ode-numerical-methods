# Euler Explicit Method – Numerical Solution of ODEs

This folder contains a MATLAB implementation of the Explicit Euler Method for numerically solving initial-value problems of ordinary differential equations (ODEs).

📁 **Repository link**: [github.com/ignaciomarquezalbes/ode-numerical-methods/tree/main/euler-explicit](https://github.com/ignaciomarquezalbes/ode-numerical-methods/tree/main/euler-explicit)

## Method Overview

The Explicit Euler Method is a first-order numerical integration technique used to approximate solutions of the form:

y'(x) = f(x, y),

y(x₀) = y₀,

It works by taking small steps along the curve using the slope provided by the differential equation. Explicitly, the algorithm 
computes successive values using:

yₙ₊₁ = yₙ + h * f(xₙ, yₙ),

xₙ₊₁ = xₙ + h,

where:
- `h` is the step size,
- `f` is the function defining the ODE,
- and `(xₙ, yₙ)` is the current point. 

## Folder Structure

- `main.m` — Entry point. Sets up the initial values and calls the solver.
- `euler_explicit.m` — Implements the Forward Euler algorithm.
- `function.m` — Defines the function *f(x, y)* for the ODE system.
- `solution.m` — Provides the exact solution *y(x)* for error estimation.
- `data.m` — Contains all problem parameters (step size, initial conditions, etc.).
- `escribe_cabecera.m` — Prints a header for formatted output.
- `escribe_paso.m` — Prints values at each step of the iteration.

> Utility scripts `escribe_cabecera.m` and `escribe_paso.m` were provided in coursework and are included here (translated to English) to handle formatted console/file output.
