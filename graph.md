# graphs

trees are graphs, doi

flow any which way, can be weighted or unweighted, directed or not

directed or undirected edges

set of vertices, set of edges

trees have n - 1 edges

g = (v, e)

weighted means edges have a cost, holler at yr graphboi dijkstra

selfedge: edge to one node. link to page on itself online. like a header link

multiedge: usually in directed for round trips

simple graph: none of either of those

can be no edges

directed max eges: n(n-1)

undirected: n(n-1) / 2

dense / sparse based on edge count

dense: adjacency matric, sparse: adjacency graph

walk: sequence of connected nodes

path: walk with no repeat nodes or edges

trail: no repeat edges

if threre's a path, there's a simple path

strongly conneted: path from anywhere to anywhere

undirected can only be connected, not strongly

closed walk: starts and ends at some spot

acyclic no cycles, like a tree

dag: directed acyclic

## implementation

two lists, vertices and edges

store references to node list in edge list, cheaper in memory, ints are best cuz they b tiny

adjaceny tough to find without storing lists of in and out edges

num vertices good for speed, not num edges

without lists, o(n) for traversal

storing vertices in adjaceny matrix much more efficient

set boolean value in each square to true if there's an edge between those two vertices

undirect is symmetrical, can only go through half the matrix

directed you gotta check 'em all

scanning for adjacency is o(n) if we know name, constant if we know index

finding if two nodes are connected constant

using hash table to store vertices and indices is faster

weighted graph use a giant number for unconnected nodes

matrices bad for sparse

