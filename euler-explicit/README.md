# Explicit Euler Method – Numerical Solution of ODEs

This folder contains a MATLAB implementation of the Explicit Euler Method for numerically solving initial-value problems of ordinary differential equations (ODEs).

📁 **Repository link**: [github.com/ignaciomarquezalbes/ode-numerical-methods/tree/main/euler-explicit](https://github.com/ignaciomarquezalbes/ode-numerical-methods/tree/main/euler-explicit)

## Method Overview

The Explicit Euler Method is a first-order numerical integration technique used to approximate solutions of equations of the form:

y'(x) = f(x, y),

y(x₀) = y₀.

It approximates the solution by taking small steps along the curve, using the slope defined by the differential equation. 
Explicitly, the algorithm computes successive values using:

xₙ₊₁ = xₙ + h,

yₙ₊₁ = yₙ + h * f(xₙ, yₙ),

where h is the step size, f is the function defining the ODE, and (xₙ, yₙ) is the current point. 

## Folder Structure

- `main.m` — Entry point. Sets up the initial values and calls the solver.
- `euler_explicit.m` — Implements the Forward Euler algorithm.
- `function.m` — Defines the function *f(x, y)* for the ODE system.
- `solution.m` — Defines the exact solution *y(x)* for optional error estimation (it must agree with the function in `function.m`).
- `problem_data.m` — Contains all problem parameters (step size, initial conditions, etc.).
- `write_head.m` — Prints a header for formatted output.
- `write_step.m` — Prints values at each step of the iteration.

> Utility scripts `escribe_cabecera.m` and `escribe_paso.m` were provided in coursework and are included here (translated to English) to handle formatted console/file output.
