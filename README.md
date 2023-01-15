# StuckWin
Development of the interactive interface of a game with simple rules and creation of two automatic game algorithms for algorithmic comparison purposes.

## Detailed Explanation
### The game
"Stuckwin" is a two-player game whose very simple rules are the following:
* the game board has 37 hexagonal cells, spread over an hexagonal-shaped board
* the game has 13 blue pawns and 13 red pawns, all identical
* one player holds the blue pawns, the other the red ones
* the blue player start the game
* each player in turn moves a pawn to a free space, located immediately in front of him. A token therefore only has a maximum of three possible destination locations
* a pawn cannot "jump" over one or more other pawns
* if when his turn comes, a player no longer has any possibility of moving his pawns, he wins the game
### The work required
This work was made over a 52 days learning and evaluation situation in groups of two. The final objective was to program the game "StuckWin" with instructions and constraints that had to be respected:
* The first part of the project had to be returned after 24 days. It was about the development of the interactive interface of the game "StuckWin". This meant we had to write given methods with precise instructions to display the state of the game, give the possible destinations for a given pawn, perform a given movement by simulating it to verify that it is playable and tell if the game is over or not.
* The second part of the project had to be returned after 52 days. It was about the design, implementation and comparison of two automatic game algorithms for the user to play against.

The instructions and constraints for the code are the following:
* each file must include a header specifying our surnames, first names, groups and possibly details relating to the work presented in the following lines
* the source code we return must be commented and as readable as possible
* each method should have its own javadoc-like documentation block
* the indentation must be rigorous (code, parentheses, brackets)
* parentheses surrounding method parameters must be sticked to the name of the method
* lines should not exceed 80 characters
### The work done
First part:
* Display of the current state of the game directly into the terminal as if it was in its hexagonal layout, since the game's state is stored in a two dimensional table of characters corresponding to a cell's state (red / blue / empty / doesn't exist), showing each one of them with their own color
* Listing of the possible positions of a pawn according to its color. If the target cell is out of the bounds of the table, it is replaced with the pawn's coordinates to prevent the game from crashing
* Verification of a movement's playability and execution according to the selected mode if it is playable
* Verification of the game's state to tell if the game is over or not (checking for each of the player's pawns if it is playable or not) and tell who won if it is over
* Verification of the player's input to prevent the game from crashing because of indexes being out of bounds of the table (part of the given skeleton that was slightly changed for this reason)

Second part:
* Creation of a "naive" algorithm playing the first movement it can
* Creation of a "starter" algorithm playing randomly unless it can get one of its pawns stuck
