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

## Examples:
### T(n) = T(n/2) + 1
T(n)= (T(n/4) + 1) + 1 
...
T(n) = T(n/2<sup>i</sup>) + i
if i == log<sub>2</sub><sup>4</sup>, T(n)=T(1)(constant) + logn

### T(n) = T(n/2) + n
T(n) = T(n/2) + n = (T(n/4) + n/2) + n = T(n/2<sup>i</sup>) + n/2<sup>i-1</sup> + n/2<sup>i-2</sup>
+...+n

T(n) = T(1) + n*(1-0.5)<sup>i</sup>/(1-0.5) , i=lgn  
T(n) = n  

### T(n) = 2T(n/2) + n

T(n) = 2(2T(n/4)+n/2) + n  = 4T(n/4) + n + n
= 4(2T(n/8) + n/4) + n + n = 8T(n/8) + n + n + n =  ....   
= 2<sup>i</sup>T(n/2<sup>i</sup>) + i*n  
i=lgn, T(n) = nlgn + n

## Guessing and Checking
### Induction (数学归纳法)
For example, assume that T(n) = T(n-1) + 1 is O(n) and T(1)=1.  
T(n) < cn.

Start at T(1), and apply to the T(2) ... and so forth. And if our solution is correct for T(n-1), 
it's true for T(n).

Assume: T(n)< cn (c>=1)
So T(n) = T(n-1) + 1= c(n-1) + 1 = cn-c+1 <= cn
### Prove divide and conquer algorithm
Assumption: T(k) <= ck * lgk  
T(n) = 2T(n/2) + n <= 2c * (n/2 * lg(n/2)) + n = c n lgn

# Master Theorem
General form:  
T(n) = aT(n/b) + f(n)  
To reach the T(n), we need log<sub>b</sub>n height tree.  
Each internal node has a children. The number of nodes incease a times each level. So the width of the tree
is a<sup>log<sub>b</sub>n</sup>. 
a<sup>log<sub>b</sub>n</sup> = n<sup>log<sub>b</sub>a</sup>  
Prove:
have ln on both side:
logbn * lna = logba * lnn  
lna/lnn = logba/logbn  is always true
