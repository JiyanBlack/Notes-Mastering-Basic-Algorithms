# Graph Terminology

1. Graph: an abstract network consists of nodes(vertices), connected by edges(arcs). A graph is a pair of sets
G = (V, E).
2. Directed Graph: edges are ordered. An edge E(u,v) is a directed line from u to v. A directed graph can have 
antiparallel edges between a and d(edges going both ways). Parallel edges(both from a to b) are not allowed.
3. self-loop: A node have a edge links to itself. Not allowed in an undirected graph, but possible in a digraph.
Convention is to disallow it.
4. An undirected graph can be simulated by directed one, just replace each undirected edge with a pair of antiparallel
directed edges(two-way edges)
5. An edge is incident on its two nodes, called its end nodes. Undirected uv s incident on u and v.
Directed uv, u is head, v is tail, it leaves(incident from) u and enters(incident to) v.
6. An edge uv, u and v are adjacent and neighbours.
7. The set of neighbors of node v is called N(v).
8. All nodes are neighborhoud to all others, is called a complete graph.
9. For directed graph, the nodes adjacent to u are those we can reach following the directions from u.
10. The size of N(v) is called its degree.
11. in-degree(incoming edges), out-degree(outgoing edges)
12. H is a subgraph of G --> G contains H
13. Spanning subgraph covers all the nodes from the original graph(edges are different).
14. Path: a sequences of nodes following the directions of the edges.
15. Cycle: A cycle is constructed by connecting the last node of a path to the first.
16. Walk: like path, but can be visited multiple times.
17. Weighted Edges: each edge is assigned a real weight number, written as w(u,v).
18. A graph is connected if it contains a path between each pair of nodes(same in digraph).
19. Connected Components: the maximal subgraphs of a graph that are connected
20. Acyclic graphs: do not have cycles.
21. Forest is undirected and acyclic graph. 
22. Tree is the connected components of a forest.
23. Nodes with degree of one are called leaves. Others are called internal nodes.
24. The following are the same:
  1. T is a tree (that is, it is acyclic and connected).
  2. T is acyclic, and has n–1 edges.
  3. T is connected, and has n–1 edges.
  4. Any two nodes are connected by exactly one path.
  5. T is acyclic, but adding any new edge to it will create a cycle.
  6. T is connected, but removing any edge yields two connected components.

# Graph Expression
## Adjancency Lists
1. [{set},{set}], e.g. N = [  
{b, c, d, e, f}, # a  
{c, e}, # b  
{d}, # c  
{e}, # d  
{f}, # e  
{c, g, h}, # f  
{f, h}, # g  
{f, g} # h  
]  
2. [[list],[list]]
3. Weighted Graph: [ {dict}, {dict} ]
4. {'a': set('bcdef'),'b':set('ce')}
## Adjancency Matrices
W = [[0,2,1,3,9,4,_,_], # a  
[_,0,4,_,3,_,_,_], # b  
[_,_,0,8,_,_,_,_], # c  
[_,_,_,0,7,_,_,_], # d  
[_,_,_,_,0,5,_,_], # e  
[_,_,2,_,_,0,2,2], # f  
[_,_,_,_,_,1,0,6], # g  
[_,_,_,_,_,9,8,0]] # h  
## Difference
The main criterion would probably be the asymptotic
performance for what you’re doing. For example, looking up the edge (u, v) in an adjacency matrix is
Θ(1), while iterating over v’s neighbors is Θ(n); in an adjacency list representation, both operations will
be Θ(d(v)), that is, on the order of the number of neighbors the node has. If the asymptotic complexity of
your algorithm is the same regardless of representation, you could perform some empirical tests, as
discussed earlier in this chapter.

# Implement Trees
Any graph implementation can be used to represent tree. But specialized tree structures can make trees easier to implement
and work with.
## Binary Tree
```python
class Tree:
  def __init__(self, left, right):
    self.left = left
    self.right = right
    You can use the Tree class like this:
>>> t = Tree(Tree("a", "b"), Tree("c", "d"))
>>> t.right.left
'c'```
