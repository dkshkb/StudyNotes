# Greed Algorithm Questions

### 1024 Video Stitching
### Set Cover  
1. Score each node/school by number of currently uncorved nodes that would be covered if we put a school there
2. Pick the node with highest score, put a school there
3. Continue until all nodes are covered

Counterexample: 

Time Complexity
- Score each node O(n), O(n^2) for all notes
- Pick max - can be done as part of the previous step
- Update covered vector O(n) **WHY**
  
Worst case: n iterations -> n * O(n^2) = O(n^3)

### [1029. Two City Scheduling](https://leetcode.com/problems/two-city-scheduling/)
sort the persons by price_A - price_B and then send the first n persons to the city A, and the others to the city B, because this way the company costs are minimal.  
Correctness: think of opportunity cost. 
