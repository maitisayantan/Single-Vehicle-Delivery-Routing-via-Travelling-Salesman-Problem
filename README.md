S**ingle Vehicle Delivery Routing via Travelling Salesman Problem**

**Project Overview**

This project focuses on solving a single-vehicle delivery routing problem in Mumbai, modeled as a Travelling Salesman Problem (TSP). The objective was to determine the shortest possible route that visits all delivery sites exactly once and returns to the starting point. The project leverages mathematical optimization techniques implemented in Pyomo, with different TSP formulations compared for efficiency.

**Problem Formulation**

The problem was formulated as a single-vehicle Precedence-Constrained Delivery Travelling Salesman Problem (PDTSP) for 19 delivery sites located across Mumbai. Distances between sites were computed using the Haversine formula to account for real-world latitude–longitude coordinates.

**Methodology**

Three classical formulations of the Travelling Salesman Problem were implemented using the CBC solver in Pyomo:

**DFJ (Dantzig–Fulkerson–Johnson) Formulation** – Subtour elimination using combinatorial constraints.

**MTZ (Miller–Tucker–Zemlin) Formulation** – Introduced ordering constraints to prevent subtours.

**3-Index Formulation **– Modeled with binary decision variables across city pairs and positions.

The travel paths were visualized on a map of Mumbai, allowing intuitive interpretation of the optimal delivery routes.

**Results**

All three formulations successfully produced feasible delivery routes.

DFJ formulation achieved the fastest solve time, making it the most computationally efficient among the tested models.

The visualization highlighted optimized routes that minimized travel distance while covering all sites.

Insights

This project demonstrates how operations research techniques can be applied to real-world last-mile delivery problems. By comparing multiple TSP formulations, it provides insights into both the mathematical structure of routing problems and the computational trade-offs between different models.
