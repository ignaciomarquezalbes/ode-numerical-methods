# Implicit Euler Method – Numerical Solution of ODEs

This folder contains a MATLAB implementation of the Implicit Euler Method for numerically solving initial-value problems of ordinary differential equations (ODEs).

📁 **Repository link**: [github.com/ignaciomarquezalbes/ode-numerical-methods/tree/main/euler-implicit](https://github.com/ignaciomarquezalbes/ode-numerical-methods/tree/main/euler-implicit)

## Method Overview

The Implicit Euler Method is a first-order numerical integration technique used to approximate solutions of equations of the form:

y'(x) = f(x, y),

y(x₀) = y₀.

It approximates the solution in a similar fashion to the Explicit Euler Method. 
In this case, the algorithm computes successive values using:

xₙ₊₁ = xₙ + h,

yₙ₊₁ = yₙ + h * f(xₙ₊₁, yₙ₊₁),

where h is the step size  and f is the function defining the ODE. 
Observe that, in contrast with the Explicit Euler Method, this is an implicit method, 
that is, the expression to compute the new approximation, yₙ₊₁, depends on yₙ₊₁ itself and,
thus, the method needs to solve an algebraic equation for the unknown. 

## Folder Structure

- `main.m` — Entry point. Calls the data for the problem and the solver.
- `euler_explicit.m` — Implements the Implicit Euler algorithm.
- `function.m` — Defines the function *f(x, y)* for the ODE.
- `solution.m` — Defines the exact solution *y(x)* for optional error estimation (it must agree with the function in `function.m`).
- `problem_data.m` — Contains all problem parameters (step size, initial conditions, etc.).
- `write_head.m` — Prints a header for formatted output.
- `write_step.m` — Prints values at each step of the iteration.

> Utility scripts `escribe_cabecera.m` and `escribe_paso.m` were provided in coursework and are included here (translated to English) to handle formatted console/file output.
