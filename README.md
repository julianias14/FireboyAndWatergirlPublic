# Fireboy and Watergirl (Recursion Assignment)
## Overview
This project is a **recursion-based assignment** developed for CS111: Introduction to Computer Science at Rutgers University — New Brunswick.

Students are asked to implement a recursive function to navigate a maze for two characters inspired by the classic _Fireboy and Watergirl_ game:
* Fireboy: can walk through lava, avoids water
* Watergirl: can walk through water, avoids lava

Both characters must also avoid green goo, and the goal is to find a safe path to the exit using recursion and conditionals. Students must implement an algorithm to explore the maze, keep track of visited paths, and determine the ultimate safe path.

I created this assignment with a peer as part of the Rutgers Assignment Guru program, where undergraduate students work to create assignments for Rutgers' CS111: Introduction to Computer Science and CS112: Data Structures classes.

### ⚠️ Note: This repository intentionally contains ***starter code only*** (with "write your code here" placeholders) to comply with academic integrity policies. The solution to the assignment is not posted in order to avoid academic integrity violations from students taking this course. However, images of the assignment are given in this documentation.

## Technologies
* Java
* Recursion & Backtracking
* 2D Arrays
* File Input Handling

## Features
* Reads a maze from an input file into a char[][]
* Tracks visited cells for each character using boolean 2D arrays
* Recursive path exploration with backtracking: attempts all valid neighboring steps
* Outputs visited paths as grids

## Maze Legend
* ‘F’ = lava; only Fireboy can step here.
* ‘W’ = water; only Watergirl can step here.
* ‘N’ = neutral; both characters can step here.
* ‘G’ = green goo; neither character can step here.

## How it Works
1. Input File
First line: maze dimension d
Next d lines: maze grid characters (F, W, N, G)
2. Initialization
Creates a char[][] maze
Creates boolean[][] fireboyVisited and boolean[][] watergirlVisited
3. Execution
Calls the recursive method nextStep() for Fireboy starting at (0,0)
Prints Fireboy's visited path
Calls nextStep() for Watergirl starting at (0,0)
Prints Watergirl's visited path
4. Recursive Method: nextStep()
Base case: returns if the current cell is out of bounds, has been visited, or unsafe for the hero
Recursive step: marks the current cell as visited, calls nextStep() on neighbors in the following order: down, left, up, right

## Running the Project
Compile: javac FireboyAndWatergirl.java
Run: java FireboyAndWatergirl <input_file>

## Example:
### javac FireboyAndWatergirl.java\n
### java FireboyAndWatergirl maze2.txt
<br>
<img width="280" height="398" alt="image" src="https://github.com/user-attachments/assets/f346e49c-bbbb-4f22-bc3c-ca318bf31e70" />

## ⚠️ Academic Integrity
This repository is intended for professional reference only. Students are expected to complete the implementation based on the description from the official course website.
