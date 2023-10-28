# 2048

*module*.*
*.classpath
*.project
*.settings

# README #

# Link to Google Doc Brainstorming: https://docs.google.com/document/d/1uw4e3GuvjMj3Ro7qlPFqAhrwx5sQvoB8kOG69g0GyZ0/edit?usp=sharing

## Group Information ##

**Team Members**
Allison Y. 
Rajvi S. 
Mira P. 

**Group Number:** 2

**Period:**	4 

**Game Title:** Life 2048

## Game Proposal ##

How to play: Use your arrow keys to move the tiles. Tiles with the same number merge into one when they touch. Add them up to reach the end (highest ranking tile).
Features: Arrow keys to move tiles, animation for smooth moving of tiles, randomizer to generate new tiles, and a storyline

Game Controls:

+ use left, right, up, and down keys to move/combine blocks

Game Elements:

+ Use arrow keys to move the tiles. Tiles with the same value merge into one when they touch. Add them up to reach the end goal
+ similar to getMIT but with a slightly different story (start with regular 2048 and improve afterward)
+ All new tiles must be one of the lowest two values
+ Tile --> holds a value of some type; there will be different rankings of tiles 
+ Grid --> holds a 2d array of tiles
+ Score board --> shows current score

How to Win:

+ The goal is to get to the highest tile by combing tiles.
+ Tiles can be combined using the arrow keys on the keyboard.
+ When a key is pressed, all the tiles will shift as far as possible in that direction until they hit a wall or another tile they cannot combine with.
+ Any two of the same tiles will combine together and upgrade themselves to the next level.
+ Once the highest possible tile the game is won.


## Link Examples ##

+ [2048](https://play2048.co/)
+ [getMIT](https://mitchgu.github.io/GetMIT/)

## Teacher Response ##

Your teacher can add comments and suggestions here

## Class Design and Brainstorm ##

Data 
  + 2D array of type Tile, to store the numbers 
  + Has methods for accessing the 2D array and generating random numbers 
  + The random numbers are generated both throughout the game and at the very beginning of the game  
  + Has an instance variable/ return method for score (current score &  highest score) 
  + Decides when the game is lost or won

Scene Class 
  + Home Screen w/ instructions 
  + Game Screen 
  + New Game Screen 

GUI/Driver Class
  + Displays the game using a Data class type (shows images)
  + User/Keyboard input for shifting tiles
  + Animation (using javafx) for the smooth transition of each tile moving onto another, etc. 
  + Updates data using methods in the Data Class

Tile Class 
  + Stores the value  and location of each tile
  + compareTo(Tile tile) method



