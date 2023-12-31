# mowitnow

We want to create an automatic mower (tondeuse à gazon) which is able to mow a rectangular area. We will use Test Driven Development (TDD) approach to develop this program.

## The grid

Consider the lawn (pelouse) as a grid of any size. It begins at 0,0 and expands to infinity. The mower is not able to go to negative coordinates.

## The mower position

The position of the mower at any moment is defined by both its coordinates on the grid (x, y) and a letter for its orientation (N,E,W or S). 

For example if the mower position is « 0, 0, N », it means that the mower is at the left bottom corner and oriented to the North (same as the grid picture above).

## The program

We initialise our program with this 2 informations :
- The initial position of the mower.
- A list of commands.

## The mower commands

The mower only knows 3 different types of commands, and treats it one after the other :
- L : rotate 90° to the Left without moving.
- R : rotate 90° to the Right without moving.
- M : Move forward, without changing orientation.

If a Move event throws the mower to negative coordinates, the mower does not move.

We expect the program to execute all the commands, then return the current mower position and orientation.

## Questions

*Question 1:* Bootstrap the project which everything you need to create your mower.

*Question 2:*  Write a first test to initialise the Mower and get its position. We will implement the Mower code only from Question 3.

*Question 3:*
Now implement your mower code to make your previous test pass.

*Question 4:* 
If we initialise the program with :
initial position : 	1 2 N
list of instructions : 	MM
we expect the result :  1 4 N

*Question 5:* 
If we initialise the program with :
initial position : 	1 2 N
list of instructions : 	RRR
we expect the result :  1 2 W

*Question 6:*
If we initialise the program with :
initial position : 	1 2 N
list of instructions : 	LLL
we expect the result :  1 2 E

*Question 7:*
If we initialise the program with :
initial position : 	1 2 N
list of instructions : 	MRMRMRMR
we expect the result :  1 2 N

*Question 8:*
If we initialise the program with :
initial position : 	1 2 N
list of instructions : 	LMMLMMM
we expect the result :  0 0 S

*Question 9:*
The next question should work out of the box, consider this initialisation :
initial position : 	1 2 N
list of instructions : 	LLMMMRRRRRMMRMMMRMLM
we expect the result :  1 4 N

## Architecture questions

- Moving from the Mower POC to a start-up, could you please explain which languages, technologies and infrastructure would you put in place to allow the management of millions of connected mowers across the world ?
