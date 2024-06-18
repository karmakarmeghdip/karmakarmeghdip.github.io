### Tractable and Intractable Problems

**Tractable Problems:**
- These are problems that can be solved in polynomial time, meaning the time required to solve the problem is a polynomial function of the size of the input.
- Examples include sorting algorithms (e.g., QuickSort, MergeSort), searching algorithms (e.g., binary search), and shortest path algorithms (e.g., Dijkstra's algorithm).

**Intractable Problems:**
- These are problems that cannot be solved in polynomial time, often requiring exponential time as the size of the input increases.
- Examples include many combinatorial optimization problems, such as the traveling salesman problem and the knapsack problem.

### Computability of Algorithms

- **Computable Problems:** Problems for which an algorithm exists that can produce a correct solution in a finite amount of time.
- **Non-computable Problems:** Problems for which no such algorithm exists. An example is the Halting Problem, which determines whether a given program will finish running or continue indefinitely.

### Computability Classes

**Class P (Polynomial Time):**
- The set of decision problems that can be solved by a deterministic Turing machine in polynomial time.
- These problems are considered efficiently solvable or tractable.
  
**Class NP (Nondeterministic Polynomial Time):**
- The set of decision problems for which a given solution can be verified as correct by a deterministic Turing machine in polynomial time.
- It is not known whether every problem in NP can also be solved in polynomial time (this is the famous P vs NP question).

**Class NP-Complete:**
- A subset of NP problems that are at least as hard as every other problem in NP.
- A problem is NP-complete if it is in NP and every problem in NP can be reduced to it using a polynomial-time reduction.
- Examples include the SAT problem (satisfiability of Boolean formulas) and the traveling salesman problem.

**Class NP-Hard:**
- Problems that are at least as hard as the hardest problems in NP.
- NP-hard problems do not have to be in NP, meaning they do not have to be decision problems.
- Examples include the Halting Problem, which is undecidable but can be used to show the hardness of other problems.

### Cook’s Theorem

- **Statement:** The Boolean satisfiability problem (SAT) is NP-complete.
- **Implication:** This was the first problem proven to be NP-complete, demonstrating that if any NP-complete problem can be solved in polynomial time, then every problem in NP can also be solved in polynomial time (P = NP).

### Standard NP-Complete Problems

- **Boolean Satisfiability Problem (SAT)**
- **Traveling Salesman Problem (TSP)**
- **Knapsack Problem**
- **Hamiltonian Cycle Problem**
- **Vertex Cover Problem**
- **Clique Problem**
- **Subset Sum Problem**

### Reduction Techniques

**Polynomial-time Reduction:**
- A method to transform one problem into another in polynomial time.
- If problem A can be reduced to problem B in polynomial time, and problem B can be solved in polynomial time, then problem A can also be solved in polynomial time.
  
**Common Reduction Techniques:**
- **Many-one Reduction (Karp Reduction):** Direct transformation of one problem to another.
- **Turing Reduction:** Using an algorithm for one problem as a subroutine to solve another problem.

### Example Reductions

- **Reducing 3-SAT to CLIQUE:**
  - Given a 3-SAT formula, construct a graph where each clause in the formula is represented by a set of vertices, and edges are added between vertices representing literals that do not contradict each other. A k-clique in this graph corresponds to a satisfying assignment of the 3-SAT formula.
  
- **Reducing CLIQUE to VERTEX COVER:**
  - Given a graph and an integer k for the CLIQUE problem, create a new graph where the goal is to find a vertex cover of size n - k. A solution to the vertex cover problem corresponds to a solution to the CLIQUE problem.