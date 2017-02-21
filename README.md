d# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: We need find naked twins first by constructing frequency table for each unit: 1. Two possible values; 2. The value combinations appears twice in the unit; Next we replace those values with empty strings for the rest cells in the unit; Using naked twins strategies, we make sure twin values are not possible solutions for the cells other than the twin cells. It helps reduce the number of possible solutions for other cells, simply search tree and might in turn speed up search in the later stage. 

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The key is to add diagonal unit to the unitlist. Once it's done, everything else could be handled using methods shown in the course. Diagonal sudoku required that numbers 1 to 9 should all appear exactly once. It's similar to the requirement for each row, column and 3x3 subsquares. By adding diagonal unit to the unit list, we are able to eliminate assigned number in the diagonal from the rest cells in the diagnoal; assign number if the number is only possible in one cell of diagonal; eliminate twin values from the cells other than twin cells in the diagnoal. 

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