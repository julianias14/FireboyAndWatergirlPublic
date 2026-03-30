# Fireboy and Watergirl (Recursion Assignment) [PUBLIC]
## OVERVIEW
This project is a recursion-based pathfinding assignment developed for CS111: Introduction to Computer Science at Rutgers University — New Brunswick.
It is inspired by the classic _Fireboy and Watergirl_ game, where each character must navigate a maze while avoiding hazards with the final goal of reaching their respective doors. Students are tasked with implementing a recursive algorithm to explore the maze, keep track of visited paths, and determine the ultimate safe path.

### ⚠️ Note: This repository intentionally contains ***starter code only*** (with "write your code here" placeholders) to comply with academic integrity policies. The solution to the assignment is not posted in order to avoid academic integrity violations from students taking this course. However, images of the assignment are given in this documentation.

## TECHNOLOGIES
* Java
* Recursion
* 2D Arrays
* File Input Handling

## Features
* Reads a maze from an input file into a char[][]
* Simulates two independent agents: Fireboy (immune to lava, avoids water) and Watergirl (immune to water, avoids lava)
* Recursive path exploration using a nextStep() function
* Tracks visited arrays with boolean 2D arrays
* Outputs traversal paths as visual grids
