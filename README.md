# Rayleigh Flow Assignment 1

## Problem 2
Reproduce the Rayleigh flow plots shown in class:

- Plot the ratios of thermodynamic properties to their respective diabatic sonic counterparts:  
  \[
  \frac{p}{p^*}, \quad \frac{T}{T^*}, \quad \frac{T_0}{T_0^*}, \; \ldots
  \]
  as functions of Mach number.
- Generate the normalized **T–s diagram** (Temperature–Entropy diagram) with appropriate scaling.

---

## Problem 3
Build on the code from Problem 2 to implement a **general Rayleigh flow solver**:

- Write a function with clear arguments and outputs that computes Rayleigh flow properties for given inputs.
- Reuse plotting routines where appropriate.
- Validate your solver by applying it to **Examples 3.13 and 3.14** from *Anderson (2003 edition)*, or two equivalent cases of your choice.  
  - Ensure both subsonic and supersonic regimes are tested.
- Compare your results against the textbook solutions for verification.

---
# Compressible Flow Assignment 2 (Fanno, Shock Interactions, Shock–Expansion)

## Problem 1 — Fanno Flow (Normal Shock Location)
Consider Example 8.3 from **Yahya** (discussed in class): a duct with a **supersonic inlet**, **sonic outlet**, and a specified **pre-shock Mach number**, where the task was to find duct lengths upstream and downstream of the shock.

Now solve the related (and more practical) problem:

- **Given:** total duct length \(L\), inlet Mach number \(M_1>1\), and sonic outlet.
- **Task:** write a program to determine the **location of the normal shock** (if it exists) within the duct.
- **Deliverables:**
  - A function that, for inputs \((L, M_1, \gamma, f)\) (and any other needed parameters), returns:
    - shock location \(x_s\) from the inlet (or a clear indication that **no physical solution** exists),
    - upstream/downstream segment lengths \((x_s, L-x_s)\),
    - key state properties upstream and downstream of the shock.
  - Show that your code **reproduces** the solution of **Yahya Example 8.3**.
  - **Discuss** any scenarios where the solver fails to find a solution and explain **why** (e.g., \(L\) too short/long for the required Fanno evolution to/from \(M=1\)).

> Tip: Structure the solver around Fanno line relations, friction parameter \(4fL/D\), and the jump conditions for a normal shock in a constant-area duct.

---

## Problem 2 — Interaction of Shocks of Opposite Families
- **Task:** implement and run a solver for **Example 6.5** from **Oosthuizen** (note: there is a **mistake near the end** of the textbook solution).
- **Deliverables:**
  - Code that computes the interaction of **opposite-family shocks** (e.g., left-running compression with right-running expansion or vice versa), including post-interaction states and wave angles.
  - A brief note identifying the **textbook error** and presenting the **corrected** result from your code.
  - **Validation:** solve **similar examples** from other references/textbooks to cross-check your implementation.


## Problem 3 — Shock–Expansion Theory (Anderson, 2003, Example 4.15)
- **Task:** code and run the **shock–expansion** solution for **supersonic flow over a flat plate** as in **Anderson (2003) Example 4.15**.
- **Deliverables:**
  - Compute and report the **lift** and **drag coefficients** \(c_\ell, c_d\).
  - Compute the **precise slip-line angle** (see **Fig. 4.37** in Anderson).
  - **Validation:** solve **similar problems** from other sources (e.g., wedge/cone flows or alternate plate angles) and compare results.
