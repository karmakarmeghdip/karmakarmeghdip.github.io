## Fundamental Algorithmic Strategies

### 1. Brute-Force
- **Definition**: An exhaustive search method that tries all possible solutions to find the correct one.
- **Characteristics**:
  - Simple to implement
  - Guaranteed to find the correct solution
  - Often inefficient for large problems due to high computational cost
- **Applications**:
  - Small-scale problems where the solution space is manageable
  - Example Problems:
    - **String Matching**: Check all substrings of the text to find the pattern.
    - **Travelling Salesman Problem (TSP)**: Calculate the total distance for every permutation of cities and choose the shortest.

### 2. Greedy
- **Definition**: Builds a solution iteratively, choosing the locally optimal choice at each step with the hope of finding a global optimum.
- **Characteristics**:
  - Often simple and fast
  - Not always guaranteed to produce the optimal solution
- **Applications**:
  - Problems where local optimality leads to global optimality
  - Example Problems:
    - **Activity Selection**: Select the maximum number of activities that don't overlap.
    - **Knapsack Problem**: Select items based on the highest value-to-weight ratio.

### 3. Dynamic Programming (DP)
- **Definition**: Solves problems by breaking them down into simpler subproblems and storing the results of these subproblems to avoid redundant computations.
- **Characteristics**:
  - Efficient for problems with overlapping subproblems and optimal substructure
  - Uses memoization or tabulation
- **Applications**:
  - Optimization problems
  - Example Problems:
    - **Knapsack Problem**: Compute the maximum value for different capacities.
    - **Fibonacci Sequence**: Store previously computed values to avoid recalculation.

### 4. Branch and Bound
- **Definition**: Systematically explores branches of a solution space, "bounding" branches that cannot yield better solutions than the current best.
- **Characteristics**:
  - Prunes large portions of the search space
  - Used for combinatorial and optimization problems
- **Applications**:
  - Problems with large solution spaces
  - Example Problems:
    - **TSP**: Prune paths that exceed the current shortest path.
    - **Knapsack Problem**: Use upper and lower bounds to eliminate infeasible solutions.

### 5. Backtracking
- **Definition**: Incrementally builds candidates to the solution, abandoning a candidate ("backtracking") as soon as it determines that this candidate cannot lead to a valid solution.
- **Characteristics**:
  - Effective for constraint satisfaction problems
  - Can be inefficient for large problems without good heuristics
- **Applications**:
  - Problems with constraints
  - Example Problems:
    - **N-Queens**: Place queens one by one and backtrack if conflict arises.
    - **Sudoku**: Fill cells one by one, backtracking when a cell placement leads to a conflict.

## Illustrations of Techniques for Specific Problems

### 1. Bin Packing
- **Greedy**: Place each item in the first bin that has enough space.
- **Dynamic Programming**: Use DP to find the optimal way to pack items, considering all bins and items.

### 2. Knapsack Problem
- **Brute-Force**: Evaluate all subsets of items to find the maximum value that fits within the weight limit.
- **Greedy**: Select items based on the highest value-to-weight ratio until the knapsack is full.
- **Dynamic Programming**: Build a table to store the maximum value for different capacities.
- **Branch and Bound**: Use upper bounds to eliminate infeasible solutions early.

### 3. Travelling Salesman Problem (TSP)
- **Brute-Force**: Calculate the total distance for every permutation of cities.
- **Greedy**: Construct a tour by repeatedly visiting the nearest unvisited city.
- **Dynamic Programming**: Use the Held-Karp algorithm to find the shortest tour.
- **Branch and Bound**: Prune paths that exceed the current best known tour length.
- **Backtracking**: Explore all possible tours, abandoning paths that cannot lead to a better solution.

## Heuristics
- **Characteristics**:
  - Provide approximate solutions quickly
  - Not guaranteed to be optimal
  - Useful for large and complex problems
- **Application Domains**:
  - Problems where exact solutions are computationally infeasible
  - Examples:
    - **Local Search**: Improve an initial solution by making local changes (e.g., hill climbing, simulated annealing).
    - **Metaheuristics**: Frameworks for developing heuristic algorithms (e.g., genetic algorithms, ant colony optimization).

These strategies and techniques provide a toolbox for solving a wide variety of algorithmic problems, each with its strengths and suitable application contexts.