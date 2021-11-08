# Dynamic Programming Lecture

Example :Shortest Paths in a DAG
- Linearize this DAG

Algorithm: 

initialize all dist(.) values to infinity     
dist(s) = 0    
for each v in V\{s}, in linearized order:  
   <a href="https://www.codecogs.com/eqnedit.php?latex=dist(v)&space;=&space;min_{(u,v)&space;\in&space;E}&space;\{dist(u)&space;&plus;&space;l(u,v)\}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?dist(v)&space;=&space;min_{(u,v)&space;\in&space;E}&space;\{dist(u)&space;&plus;&space;l(u,v)\}" title="dist(v) = min_{(u,v) \in E} \{dist(u) + l(u,v)\}" /></a>

