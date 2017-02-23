# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Naked Twins are pairs of candidates in two cells belonging at least to one unit
(row,column or block). Each of the pairs candidate can ony exist in the one or the other cell. 
Consequently those candidates can be removed from all other cells in this unit. 
The constraint propagation technique applies as we repeat the method until the solution is found (or not). 
Like in the Elimination method or in the "Only Choice" method, in the "Naked Twins" method we can aplly the 
constraint propagation until find a solution or a better position to achive the solution. Then we can aplly
other methods until a solutions is found. 

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The Diagonal Sudoku has an additional constraint compared to other methods. Additionally to the row, column 
and block constraint, we have also the 2 diagonal lines constraints. 
To incorporate constraint propagation in the diagonal solution, the best way is to create two new units, 
with the individual elements of the two diagonals. This new units will introduce new constraints in the system, 
who will be resolved normally with elimination, only choice or search methods.
This will result in not accepting solutions that do not satisfy the diagonal constraint. When all the 
constraint disappear the problem is resolved.  


### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.