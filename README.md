# 🧩 Latin Square CSP Solver

> A Python-based Constraint Satisfaction Problem (CSP) solver designed to complete partially filled Latin squares. Developed as a university laboratory project for the "Intelligent Systems" course.

This repository demonstrates how to apply classic Artificial Intelligence search algorithms and constraint propagation techniques to solve complex combinatorial grids. 

---

## 🚀 Core CSP Algorithms & Heuristics
The solver optimizes the standard backtracking approach by integrating several advanced heuristics to prune the search tree dynamically:
- **Minimum Remaining Values (MRV):** Selects the next unassigned variable that has the fewest valid options remaining in its domain.
- **Degree Heuristic:** Acts as a tie-breaker for MRV, selecting the variable that shares the most constraints with other unassigned variables.
- **Least Constraining Value (LCV):** Evaluates and orders domain values based on their impact, prioritizing values that leave the maximum flexibility for neighboring variables.
- **Forward Checking:** Proactively updates the domains of related unassigned variables immediately after an assignment, failing early if any domain becomes empty.

---

## ⚙️ Key Features
- **Strict Latin Square Constraints:** Automatically enforces the rule that every number from $1$ to $n$ must appear exactly once per row and once per column without conflicts.
- **Procedural Grid Generation:** Features a built-in generator (`generate_partial_latin`) to create solvable, random partial Latin squares based on a specified number of initial clues.
- **Interactive CLI:** Users can input their own custom grids row-by-row or request an automatically generated puzzle via the command-line interface.
- **Performance Metrics:** Tracks and outputs the total execution time, number of assignments, and backtrack count to benchmark the algorithm's efficiency.