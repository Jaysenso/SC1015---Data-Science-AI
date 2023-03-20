# SC1015---Data-Science-AI

/b Breadth First Search Algorithm \b
breadth first search algorithm is complete but is not optimal. BFS will always find a solution if one exists but since it does not take into account the cost of the path from the start state tot he curent state, in other words, BFS will find the shortest from the start state to the goal state only if all edge costs are equal.

Ways to increase efficiency:
1. Implementing an iterative deepening search: An iterative deepening search limits the depth of the search at each iteration and gradually increases the depth limit. This technique ensures that BFS does not expand nodes beyond a certain depth, reducing the search space.

2. Applying heuristics: Heuristics can be applied to the BFS algorithm to guide the search towards the goal state. However, this may compromise the completeness of the algorithm.




Death First Search Algorithm is not complete because the algorithm may get stuck in an infinite loop if there is a cycle in the graph. This means that our algorithm may not be able to find a path even if one exists.

In addition, it it not optimal because DFS does not guarantee that the found path is the shortest path.

Ways to increase efficiency:
1. implement backtracking to void exploring unnecessary paths -> this means that if the search reaches a dead end, we can backtrack to the last node with unexplored neighbors and continue the search from there.




UCS is complete because it explores all possible paths from the initial state to the goal state, and eventually finds the optimal solution if one exists. However, UCS is not necessarily optimal because it does not take into account the heuristic information about the problem domain, such as the distance between the current node and the goal node

ways to improve efficiency:
1. using a heuristic function: to guide the search towards the goal state




The greedy search algorithm is not complete because it can get stuck if the heuristic is not admissible.  If the heuristic is not admissible, the algorithm can overlook the optimal path and return a suboptimal path, since it did not overestimates the actual distance to the goal node. 

It is not optimal too because it only consider the heuristic value and not the actual path cost when selecting nodes to explore, this might lead to what we have previously mentioned, suboptimal path caused by non-admissible heuristic value. 

Ways to increase effiiciency:
1. Using A* search algorithm, an extension of greedy-search that only uses heuristic value to select node to explore. A*star search algorithm uses both actual path cost and heuristic value to select nodes to explore. It guarantees that the optimal path will be found if the heuristic is admissible.




A* search algorithm is both complete and optimal under certain conditions.

A* is complete if a solution exists and the cost of that path is finite, A* will be able to find it.

In addition, A* search algorithm is optimal if the heuristic function used is admissible, meaning it doesnot overestimate the true cost to the goal. if heuristic value is admissible, then A* search is guanranteed to return the shortest path from start to the goal.


Ways to increases efficiency:
