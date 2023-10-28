Allison Yu 

Period 4


Friday, May 6th (in class) - 1 hour 30 mins

Today we finished making a new branch and moving our ArcadeEngine files into it. We also finished brainstorming our game and added it to 
the readme file.



Wednesday, May 11th (in class) - 45 mins

Today we finished making a basic Tile class, GameWorld class, and Game class. We had a bit of trouble trying to figure out how we would structure the base of 
our game but we eventually just made a GameWorld class which would take care of the GUI portion, the Game class which would actually initiate the game, and 
we would use a 2D array of Tile objects. We also decided to use just a Pane for our 2048 board. Initially we thought we would use a GridPane but soon realized
that it would be very difficult to do the animations of the tiles moving around. We also got a tile to show up on the screen. Next time we will start coding
the actual game logic and the controls. We took a bunch of screenshots of standard 2048 tiles and added them as Images. 



Friday, May 13th (in class) - 1 hour 30 mins

Today we started adding more details to our classes. Early on we realized that there were a lot of changes we had to make to the overall structure of our game.
Our original setter for the Tile value and image were separate, but we ended up just making it one method called setImg(int val) where you could pass in 
the new value for the tile and it would automatically change the image of the tile to match the value passed in. That way, it would be a lot easier to use (more 
flexible). We also formatted our grid for the 2048 game. It isn't centered on the pop-up window but we decided to just leave it for later. We got the random
generation of two base tiles to work. We also started coding the key input to move the tiles. Once we finish that, all we have left is adding two of the same 
tiles together and the random generation of one tile in an empty spot on the grid.


Tuesday, May 18th (in class) - 1 hour 30 mins
We fixed some errors we had in the Game Over code because it would end when the entire grid was filled even if there were tiles that could be combined.
We also added the Game Won code and centered the board. We added background images to the board.


Wednesday, May 18th (in class) - 45 mins
In class, we tried to figure out how to add animation. We added dx and dy attributes to the tile and modified the act method so that it calls move by dx and dy.
We also added setters and getters for attributes.


Friday, May 20th (in class) - 1 hour 30 mins
We fixed some errors with animation. Tiles were jumping to their location after moving by animation by one tile so we had to change a few things so that it would
work accordingly. We started the combining code with animation. It works most of the time, but there are still some bugs we need to figure out. When we move/combine
the tiles, we do it in the wrong order because the tile we are combining with disappears before the other tile reaches it. We will need to work to fix that later.

Tuesday, May 24th (in class) - 1 hour 30 mins
We had an issue with our animation where we would be able to see the dark gray background for a moment before the new tile would move to its designated position.
To fix this, we decided to just add the blank tiles to the background so that whenever a tile with an actual value was moved, its old position will already be
filled with a blank tile. This made coding the animation a lot easier, but we had to adjust a couple of things in our base code because of this change.

Thursday, May 26th (in class) - 1 hour 30 mins
We finished animation so we started adding more GUI features and just making our game look better overall. We added the title, a score keeper, and two buttons
to generate a new game and to provide game instructions. They don't work yet, but we divided up the work so that each person can do their own part by themselves.
We ran into an issue where if we moved all of our tiles up using the up key, all of the other movements would stop working. After asking McLeod, we learned that
it is because the command of pressing the up key could have been for the buttons and gotten everything confused. So, Raji requested focus inside the arrow
key method each time we move. After we fixed that, I coded the pop ups for the game over, game won, and game instructions. Mira coded the new game and score
keeping.

