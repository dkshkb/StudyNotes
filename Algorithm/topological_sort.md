# Topological Sort (Linearization)

**Topological Sort** is to find a global order for all nodes in a DAG (Directed Acyclic Graph) with regarding to their dependencies.

 - There is always a possible topological sort for DAG (Directed Acyclic Graph)

 Algorithm:

```
L = Empty list that will contain the sorted elements
S = Set of all nodes with no incoming edge

while S is non-empty do
    remove a node n from S
    add n to tail of L
    for each node m with an edge e from n to m do
        remove edge e from the graph
        if m has no other incoming edges then
            insert m into S

if graph has edges then
    return error   (graph has at least one cycle)
else 
    return L   (a topologically sorted order)
```


Leetcode: 
- 207. Course Schedule

