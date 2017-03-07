# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: 
The naked twins should be approached by looking at each boxes includes same two possible digit values in the same unit(row,column,square or newly added diagonal). If there are two boxes in accordance with this definition, these 2-digit values should be removed from other boxes in the same unit. Because there is no possibility occurrence of these digit values in other boxes of unit.  After this operations, new boxes with 2- digit values may be formed due to pruning of boxes.  So, this operation should be iterative until we could not find any new twin boxes. 

Technically, we minimize domain of each variable by removing inconsistent values to create arc consistency.  

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: 
With diagonal sudoku, we actually defined additional constraint.  Diagonal sudoku looks for the extra units:

1.  Boxes on the line from upper left hand corner to lower right hand corner 
2.  Boxes on the line from upper right hand corner to lower left hand corner 

These will be called “units” as column units,row units or square units. We use the diagonal constraints to reduce the possible values for box variable.   

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
