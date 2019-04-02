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
