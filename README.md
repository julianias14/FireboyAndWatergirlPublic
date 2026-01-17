# FireboyAndWatergirlPublic
Recursion assignment for CS111 (Introduction to Computer Science) classes at Rutgers University - New Brunswick. The characters recursively seek a path, inspired by the classic game of the same name. Students are meant to implement a recursive function using conditionals to check for safe paths forward while keeping track of visited paths.

## OFFICIAL ASSIGNMENT DESCRIPTION:
In this assignment, you will implement a recursive function using conditionals to check for safe paths forward. This assignment simulates the Fireboy and Watergirl game, and your program is meant to find a safe path by checking for any hazards and if so, moving the character back until they can find another path forward. This pattern continues until both characters find the exit.
In the original Fireboy and Watergirl game, both characters have hazards to avoid and diamonds to collect. In your program, both characters must avoid the green goo. Fireboy can walk through lava and will collect fire diamonds but must avoid water. Watergirl can walk through water and will collect water diamonds but must avoid lava.

### main()
The input file contains the maze’s dimension d in the first line and d lines with d characters:
‘F’ = lava; only Fireboy can step here.
‘W’ = water; only Watergirl can step here.
‘N’ = neutral; both characters can step here.
‘G’ = green goo; neither character can step here.

This function reads in the input file to create the char[][] maze array. 
It also creates two arrays:
fireboyVisited: boolean 2D array to represent fireboy’s visited path.
watergirlVisited: boolean 2D array to represent watergirl’s visited path.

Then, it calls nextStep() for Fireboy and then for Watergirl.
Calls the nextStep method for Fireboy printing Fireboy’s final path.
Calls the nextStep method for Watergirl printing Watergirl’s final path.

### nextStep()
This is a recursive function that determines if the current cell (row, col) can be visited by the hero, and then visits the neighboring cells. The nextStep method returns when no other step can be taken.

A cell can only be visited once.
If a cell (r,c) has already been visited, then collectedDiamonds[r][c] is true.

Base case - the nextStep method returns when no other step can be taken:

1. The hero input will be FIREBOY or WATERGIRL.
2. The maze array is used to determine if the hero can step in the current cell (row, col) according to the following rules:
  a. ‘F’ = lava; only Fireboy can step here.
  b. ‘W’ = water; only Watergirl can step here.
  c. ‘N’ = neutral; both characters can step here.
  d. ‘G’ = green goo; neither character can step here.
3. Ensure that (row, col) are within the maze array bounds.
4. Ensure that (row, col) has not been visited yet. If the current cell (row, col) has been visited, then collectedDiamonds[row][col] is true.
5. If the current cell (row, col) cannot be visited, return.

The recursive step - the nextStep method attempts a step until no other step can be taken.

1. Take the step, mark collectedDiamonds[row][col] true.
2. Call nextStep() four times on neighboring cells in the following order:
  a. Down: the cell immediately down the current cell.
  b. Left: the cell to the left of the current cell.
  c. Up: the cell above the current cell.
  d. Right: the cell to the right of the current cell.
