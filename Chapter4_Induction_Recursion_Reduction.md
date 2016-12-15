# Reduction 
Reduction means transforming one problem to another. We normally reduce an unknown problem to one we know how to solve. The reduction may involve transforming both the input (so it works with the new problem) and the output (so it’s valid for the original problem).

# Induction
Induction (or, mathematical induction) is used to show that a statement is true for a large class of objects (often the natural numbers). We do this by first showing it to be true for a base case (such as the number 1) and then showing that it “carries over” from one object to the next (if it’s true for n–1, then it’s true for n).

# Recursion
Recursion is what happens when a function calls itself. Here we need to make sure the function works correctly for a (nonrecursive) base case and that it combines results from the recursive calls into a valid solution.

# The Celebrity Problem
In a crowd of people, the celebrity knows no one, but everyone else knows 
the celebrity. Find the celebrity.  
* Analysis: Find a node in a directed graph that points to no one and every other node
point to it.
* Solution1: Brutal force: for each node, iterate through other n-1 nodes. 
Need quadratic running time.
* Solutoin2: if G(u to v), then u is not a celebrity(reduce u in the candidates)
 and u doesn't point to !v, so reduce all non-v in the candidates.
 
 # Topological Sorting
