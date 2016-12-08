# A Tale of Two Tournaments
## Shaking Hands
Round-robin tournaments / n people shaking hands with each other / how many edges are there in the complete graph.

n(n-1)/2, O(n<sup>2</sup>)

## knockout system:
number of matches:

n/2 + n/4 + n/8 +...1  
1+2+4+...n/2  
f(n)=a<sub>1</sub> q<sup>n-1</sup>  
sum of f(n) = a<sub>1</sub>(1-q<sup>n</sup>) / (1-q)  


# Recursions
Recurrence General Form:  
T(n) = a * T(g(n)) + f(n)  
* a: number of recursive calls
* g(n): the size of each subproblem to be solved
* f(n): extra work done each call besides the recursive part

