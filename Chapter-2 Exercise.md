# 2-1
Because [[0]*10]*10 would just produce one list and repeat 10 times. If one value is modified in one of the list, all
others would be changed.

# 2-2
## Array
If just use basic array data structure, three arrays are needed. A(original data array), B(B[i]=m), C(C[m]=i) and 
m(how many entries are setted.) Everytime a ith value is initialized in A, m+=1, C[m]=i, B[i]=m. To check whehter ith 
entry in A is initialized, just get m from B[i] and check if C[m]==i.
## Set
Use python built-in set data structure.
B= set(), every time ith entry is initialized in A, run B.add(i). To check if the ith entry is intialized, use
"i in B".

# 2-3
If f is O(g), then there is a postive constant c that enables f <= c*g, so g >= (1/c) * f. The definition of omega is 
there is a postive constant m that makes g >= m* f, in this case, m is 1/c.
As a result, if f is O(g), then g is omega(f)

# 2-4
log b n = (log a n)/(log a b) is true. In this case, the base can be changed and a new constant(log a b) need to be
multiplied. This is why we don't care about the base of the logarithmic algorithm. 

# 2-5

k<sup>n</sup>/n<sup>i</sup> = n logk / i logn. So k<sup>n</sup> dominates the polynomial.

# 2-6 
n<sup>k</sup> dominates any logarithm: k*lg n / lg(lg n). Because lg n always increases much faster than lg(lg n), the
former dominates the latter.

#2-7

Lists:
```
                               Complexity
Operation     | Example      | Class         | Notes
--------------+--------------+---------------+-------------------------------
Index         | l[i]         | O(1)	     |
Store         | l[i] = 0     | O(1)	     |
Length        | len(l)       | O(1)	     |
Append        | l.append(5)  | O(1)	     |
Pop	      | l.pop()      | O(1)	     | same as l.pop(-1), popping at end
Clear         | l.clear()    | O(1)	     | similar to l = []

Slice         | l[a:b]       | O(b-a)	     | l[1:5]:O(l)/l[:]:O(len(l)-0)=O(N)
Extend        | l.extend(...)| O(len(...))   | depends only on len of extension
Construction  | list(...)    | O(len(...))   | depends on length of ...
```
For linked list, the list.extend would be O(1). Because only the former_list.tail=latter_list.head need to be set up.

#2-10
A tree has n leaves, what's the internal nodes m?
```python
m*0.5 + m* 0.25 + m*0.125 +....1
```
Or a neater solution
```python
m=n-1
```
How to get it:
```
m=n/2+n/4+n/8+...1= n(1/2+1/4+...1/n)=n(1-1/n)=n-1
```
