# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: We first created a new function that will apply the naked twins elimination to the grid. This function ensures that we satisfy the naked twins constraint that no squares in the unit outside the two naked twins squares can contain the twin values. We then add a call to this function from the reduce_puzzle() function along with the other strategies. This is where the new constraints will be iteratively applied until all constraints have been satisfied. This iteration is important because applying the naked twins strategy could change the puzzle to a state where new eliminations, only choices, or even new naked twins become possible.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Diagonal Sudoku introduces two new units to the list of units that must be solved. This is done by simply adding a new unit for the top left to bottom right diagonal and another unit for the bottom left to top right diagonal to the list of possible units. As a result, boxes on the main diagonals now belong to four units while the center box belongs to five. The elimination, only choice, and naked twins strategies will automatically enforce the additional constraints introduced by the new units.

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