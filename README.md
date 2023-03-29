# AI-in-game-playing-Sokoban-Solver
## **Modeling and state** 
The game of sokoban can alternatively be considered as a search problem where we essentially look out for boxes and storage locations. So, it has it has valid start state and end state. The start state is the layout of initial puzzle whereas the end state is the state when all the boxes are tranferred to proper storage locations. The action that can be moving in all directions which lead to successor state. For modeling this game, we have standard notation that is used to independently and distinctly distinguish between all the objects in the game. Each level is given unique representation. The input for modeling consist of the following characters: ‘#’, ‘ ’, ‘&’, ‘B’, ‘.’, ‘X’. Each of these characters have special attribute of the game assigned to it: 
‘ ’ is a free space, ‘#’ is a wall, ‘&’ is player, ‘B’ is a box, ‘.’ is a goal, ‘X’ is for Sokoban on goal.
##	**Valid action**
The player can move horizontally or vertically (four directions – Up, Down, Left, Right). The player can push at most a single box into an empty space that is not a wall or an other box. The player is not allowed to pull the boxes too
##	**Successor function** 
###	**Depth First Search (DFS)**
- Depth Fist Search (DFS) is a special case of backtracking search algorithm. The search starts from the root and proceed to the farthest node before backtraking. 
- This algorithm consumes Ο(bm) time but occupies only Ο(bm) space, which is linear.  
###	**Breadth First Search (BFS)**
- Breadth First Search (BFS) is an algorithm for traversing or searching a tree or a graph structure. Generally, a search begins at a node which marked as root, and start exploring all its neighbors/successor at the same level before it moves on to the state on the next level. A BFS always complete in the sense that applying its level-by-level check, it will never miss a solution.
-The time and space complexity for BFS is Ο(bd), so the program may take much time to process and can easily go out of heap memory space. 
###	**Uniform Cost Search (UCS)**
-Uniform Cost Search (UCS) is a tree/graph search algorithm related to breadth first search. However, different from BFS which adds a state’s successor sequentially, a UCS keeps a prority queue which puts states with fewer costs in front. BFS will yield a path to the goal with least number of steps, whereas UCS will result in a path that has lowest cost.
##	**Results**
The performances of all algorithm are calculated based on standard metrics like the time consumed, solution steps.
