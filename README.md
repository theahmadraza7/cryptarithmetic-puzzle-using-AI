# cryptarithmetic-puzzle-using-AI

Problem Name :  Cryptarithmetic puzzle   

Front End: 

Using  tinker library


Running Time Complexity:
Brute Force Algorithm:
•	Let n be the number of unique letters in the puzzle.
•	Generating all permutations of n digits takes O(n!) time.
•	Checking each permutation for validity and evaluating the puzzle equation takes O(n) time.
•	Therefore, the overall time complexity is O(n!×n).
Constraint Satisfaction Problem (CSP) Algorithm:
•	The time complexity of the CSP algorithm depends on the efficiency of constraint propagation and backtracking.
•	In the worst case, if backtracking explores all possibilities, the time complexity is exponential.
•	Let n be the number of unique letters in the puzzle.
•	The worst-case time complexity is exponential, O(bn) where bb is the branching factor.
Space Complexity:
Brute Force Algorithm:
•	The space complexity is primarily dominated by the storage of permutations and assignments.
•	Since the algorithm generates all permutations, it requires additional space proportional to the number of permutations.
•	Therefore, the space complexity is O(n!).
Constraint Satisfaction Problem (CSP) Algorithm:
•	The space complexity is determined by the storage of assignments and the recursion stack during backtracking.
•	Since the recursion depth can reach the number of unique letters n, the space complexity is O(n) for the recursion stack.
•	Additional space may be required for storing assignments and other data structures used in constraint propagation.
•	Therefore, the overall space complexity can vary depending on the implementation but tends to be O(n) or higher.

Problem Formulation and Search Strategy Analysis:
Problem Description:
Cryptarithmetic puzzles involve deciphering arithmetic equations where digits are represented by letters. The objective is to find the digit-letter mappings that satisfy the equation's constraints. For example, in the puzzle "SEND + MORE = MONEY", each letter represents a unique digit, and the task is to find the correct assignment of digits to letters such that the equation holds true.
Formulating the Problem:
1.	State Space: The state space consists of all possible assignments of digits to letters. Each state represents a potential solution to the puzzle.
2.	Initial State: The initial state is the puzzle itself, with letters representing unknown digits.
3.	Actions: The actions involve assigning digits to letters.
4.	Transition Model: The transition model updates the current assignment with a new digit-letter mapping.
5.	Goal State: The goal state is reached when the assignment satisfies the puzzle equation.
Search Strategies:
1.	Brute Force Algorithm:
o	Strategy: Generate all possible permutations of digits and check each permutation for validity.
o	Advantages: Simple to implement, guarantees finding a solution if it exists.
o	Disadvantages: Inefficient for large puzzles due to exponential time complexity.
2.	Constraint Satisfaction Problem (CSP) Algorithm:
o	Strategy: Utilize constraint propagation and backtracking to efficiently explore the search space.
o	Advantages: Can handle larger puzzles more efficiently compared to brute force.
o	Disadvantages: May still be inefficient for highly constrained or complex puzzles.
Observations and Comparison:
•	Brute Force:
o	Time Complexity: O(n!×n) where nn is the number of unique letters.
o	Space Complexity: O(n!)
o	Observation: Exponential time complexity makes it impractical for large puzzles.
•	CSP Algorithm:
o	Time Complexity: Exponential in the worst case but more efficient due to constraint propagation and pruning.
o	Space Complexity: O(n) or higher, depending on implementation details.
o	Observation: Handles larger puzzles more efficiently but may still struggle with highly constrained scenarios.
Conclusion:
•	Best Algorithm: The CSP algorithm is generally more efficient for solving cryptarithmetic puzzles, especially for larger and more complex instances. It utilizes domain-specific constraints to guide the search process, resulting in faster convergence to a solution compared to brute force.
•	Recommendation: For solving cryptarithmetic puzzles, the CSP algorithm is the preferred choice due to its ability to handle larger instances more efficiently. However, for smaller puzzles or cases where efficiency is not a concern, the brute force algorithm provides a straightforward solution.

