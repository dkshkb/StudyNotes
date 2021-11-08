# Dynamic Programming Lecture

## Example
### Shortest Paths in a DAG
- Linearize this DAG

Algorithm: 

initialize all dist(.) values to infinity     
dist(s) = 0    
for each v in V \ {s}, in linearized order:  
      <a href="https://www.codecogs.com/eqnedit.php?latex=dist(v)&space;=&space;min_{(u,v)&space;\in&space;E}&space;\{dist(u)&space;&plus;&space;l(u,v)\}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?dist(v)&space;=&space;min_{(u,v)&space;\in&space;E}&space;\{dist(u)&space;&plus;&space;l(u,v)\}" title="dist(v) = min_{(u,v) \in E} \{dist(u) + l(u,v)\}" /></a>

(That's a bottom-up approach)    
We can also implement top-down DP   
storing value: memoization 


### Finding the longest increasing subsequence

- Given a sequene of numbers, we want to find the longest increasing subsequence 

5 2 8 6 3 6 9 7  

1. Create a DAG 
2. Longest path on the graph

### Shortest Path in a DAG
- DP
- Find Solutions to subproblems
- Use subproblems to find solutions to larger problems
Four possibilities
1. Fixed start, fixed end
2. Fixed start, end anywhere
3. Start anywhere, fixed end
4. start anywhere, end anywhere

#### Path Beginning Anywhere
L(i) = longest path ending at node i  
All L values = infinity  
L(1) = 0  
for v = 2:n   
   L(v) = max_{(u,v) \in E} {L(u) + w(u,v)}  
return max{L(v)}
