# Greedy Algorithm

**Minimum Spanning Tree** in an undirected, weighted graph is the spanning tree with minimum weight

Application: Cheapest way to make sure everything is connected / covered

## Finding Minimum Spanning Trees: Kruskal's Algorithm

1. sort the edges from least cost to greatest cost
2. Add each edge in order to the spanning tree, unless it would make a cycle

```
algorithm Kruskal(G) is
    F:= ∅
    for each v ∈ G.V do
        MAKE-SET(v)
    for each (u, v) in G.E ordered by weight(u, v), increasing do
        if FIND-SET(u) ≠ FIND-SET(v) then
            F:= F ∪ {(u, v)} ∪ {(v, u)}
            UNION(FIND-SET(u), FIND-SET(v))
    return F
```

Corretness (by contradiction)
- Spanning
- Tree: connected acyclic graph
- Minimum
    - Soppose Kruskal's finds tree T, which is not MST. Let T* be real MST. T $\neq$ T*
    - Let e be the lightest edge that is in T* but not in T
        - Remove e from T*, this splits T* into 2 components
        - Look at all edges in G that connect those 2 components
        - 
    - Now consider what K's model does, at some point, it has not encountered any of the other edges in x. At this point, K's will add f. Either f = e, which is a contradiction because we defined e so that is was not added by K's. Or f $\ne$ e, but then 

(The proof only applies to the case: each edge has different weights)

## Prim's Apgorithm

1. Initialize a tree with a single vertex, chosen arbitrarily from the graph.
2. Grow the tree by one edge: of the edges that connect the tree to vertices not yet in the tree, find the minimum-weight edge, and transfer it to the tree.
3. Repeat step 2 (until all vertices are in the tree).

## Huffman Encoding

Encode a string of characters using binary  
To represent k characters, we need $log_2k$ digits assuming each char is encoded by the same length of digit

Use fewer digits for more frequent characters

How to avoid ambiguous

Solution: NO char encoding is a prefix of any other char's encoding

Example
- A: 0
- B: 100
- C: 101
- D: 11

The length of the encoding of a char: depth in encoding tree

$`f_i`$: frequency of char i
 
cost of tree = $`\sum f_i`$ * (depth of ith symbol in the tree) 

The total cost of a tree is the sum of the frequencies for all leaves and internal nodes, except for the root

Infrequent: deeper in the tree
Frequent: 

Idea: find the twp chars that are least frequent, make them children of a new internal node

[Huffman Tree - Goole Interview](https://leetcode.com/problems/encode-and-decode-tinyurl/discuss/867053/huffman-tree-based-solution-java)

222. Count Complete Tree Nodes
