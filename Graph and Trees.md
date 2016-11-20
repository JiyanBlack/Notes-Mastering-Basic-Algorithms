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
