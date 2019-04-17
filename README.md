# 8Puzzle AI Project1 (University project assignment)
Solving 8 Puzzle problem using A*
### Project members:
Berkant Güneş 20160807013
### Definition of 8puzzle project:

Write a program to solve the 8-puzzle problem using the A* search algorithm. The 8-puzzle
problem is a puzzle invented by Noyes Palmer Chapman in the 1870s. It is played on a 3-by-3
grid with 8 square blocks labeled 1 through 8 and a blank square. Your goal is to rearrange the
blocks so that they are in order, using as few moves as possible. You are permitted to slide
blocks horizontally or vertically into the blank square. The following shows a sequence of
legal moves from start state to goal state.

![](http://www.cs.princeton.edu/courses/archive/spr18/cos226/assignments/8puzzle/4moves.png)

To solve the puzzle from a given search node on the priority queue, the total number of moves
we need to make (including those already made) is at least its priority, using either the
Hamming or Manhattan priority function.

There are two priority functions for this problem;
### Heuristics Options:
**Hamming priority function**. The number of blocks in the wrong position, 
plus the number of moves made so far to get to the search node. 
Intutively, a search node with a small number of blocks in the wrong 
position is close to the goal, and we prefer a search node that have been
reached using a small number of moves.

**Manhattan priority function**. The sum of the Manhattan distances 
(sum of the vertical and horizontal distance) from the blocks to their
goal positions, plus the number of moves made so far to get to the search
 node.
 
 Example(Hamming-Manhattan):
 ![](http://www.cs.princeton.edu/courses/archive/spr18/cos226/assignments/8puzzle/hamming-manhattan.png)
 
Program Structure:

The program consists of two Classes:

Board.java:Content class Board - a nxn matrix, initiate with a nxn table of int (int[n][n])

Solver.java:The main class,problem solver use A* algorhithm, input a Board(Board board), and output a solution

->Ready puzzles are included in the examples file.

### Simply program flow:
The intuitive functions used in the program are mentioned above.The priority queue of these functions is provided with the MinPQ data type in the 'algs4' library.The program first reads the puzzle from the .txt extension in the examples and first looks at its solvability.The puzzles that can then be solved reach the goal state with minimal moves using the twin swap left right etc. with the heuristic functions in the Board.java class and shows the number and steps of the moves as the output

### Conclusion:
In cases where the 8puzzle problem is solvable, the result can be reached more quickly with intuitive search methods.
When we consider the solution of the problem with real intelligence, we can see that there is also an intuitive search, the move that is estimated to be closer to the solution is generally the next move. In this context, intuitive search methods with artificial intelligence can be considered as simple modeling of search with real intelligence.
### 8-puzzle state space:
![stateSpace](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/puzzle-1.jpg)
### Output:
![output](https://github.com/brknt/8puzzle-AI-Project1/blob/master/goalstate.JPG)
