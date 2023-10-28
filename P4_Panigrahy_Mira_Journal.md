Mira Panigrahy
Period 4

Wednesday, May 11 (in class) 45 min

Today Allison and I sorted out the base code in class. We created a Tile class that extended actor to represent the tiles in 2048. We also made the Game where the entire game would run and the GameWorld which extended world and had a 2D array of tile objects within them. We downloaded images of all the tiles we would need for the game and managed to display one tile on the screen. The coding for this day was done on Allison's laptop.

Friday, May 13 (in class) 1 hour 30 min

Using the tile class and the 2D array of tiles in GameWorld, we got the screen to diplay all 16 blank tiles. We wrote to code in the OnDimentionsInitialized method to randomly create 2 non blank tiles at the start of the game. We also decided to start the key movement. This meant that as a key was pressed, all the non blank tiles would move as much as they could in that direction. This was a bit complex since the tiles had to move in a spcified order depending on the direction so that they wouldn't end up overlapping each other. The idea was that we would find the location a tile should be moved to and change the images of the tiles at those locations to make it seem as if the tiles had moved. All of the coding for this day had been done on Rajvi's laptop.

Friday, May 13 (at home) 1 hour

I completed the tile movement for the left and right keys but instead of moving them in their respective directions they moved up and down. I decided to push the code. After that, Allison figured out that the rows and columns had been switched for some reason and used that information to write the code for the left and right keys while transferring my code to the up and down keys. After this we had the basic movement for all 4 keys working.

Saturday, May 14 (at home) 1 hour

I decided to do the code to generate a new tile every time a key was pressed. It was similar to the starting code to generate a tile but it was done in the key movment class. I had to make sure that the new tile would not generate at the same location as an already placed tile. Through the process, I also figured out that the game would be over if there are no more places left to generate tiles, so I created a game over variable to keep track of when the game could be played to avoid it from crashing.

Sunday, May 15 (at home) 45 min

Our next step was to work on the combining of the tiles. We all met over zoom and helped Rajvi write the code for the combining of the tiles. When a tile is moving towards a tile of the same value, we would change the image of the destination tile to double the value. Rajvi applied to code to all 4 keys but we realized that sometimes tiles would tripple combine. For example a 2 and 2 would make a 4 and it would combine with another 4 to make a 8 in one move when those should have been 2 seperate moves. So, I came up with the idea to keep track of whether a tile has been combined already and we implemented it. After that we pushed the code to the main branch since our base code was basically done.

Tuesday, May 17 (in class) 1 hour 30 min

In class we realized that there were some issues when it came to checking when the game was over. Previously I had set the game to be over when the entire gird was full. But when we implemented the combine code we should have made it possible to combine tiles even if the grid was full and the game techinically wouldn't be over. So in class we fixed the game over code and detected if there were no more tiles that could be combined to truly declare game over. We also added a game won variable which checked if a 2048 tile was made to declare game won. This code was done on Rajvi's laptop. In class we also centered the grid and added a background image. At this point we had truly completed our base code. 

Wednesday, May 18 (in class) 45 min

Now that we had finished the basic code, we decided to start on the animation. In the actual game, the tiles would slide over to the direction they were going rather than just appear there. As I started brainstorming, I realized this would be a lot harder than we had orginally thought since would would have to alter our entire base code. Originally, the phsyical tiles wouldn't move just their images would change. But now that we wanted animation, we needed to physically move the tiles. Essentially, the array positions of the tiles couldn't match the tile at that respective position anymore since the tiles would be moving. I came up with an idea to create another array the could represent the actual postions of the tiles in the grid. Since I had planned out most of what to do, I decided to try to get the animation to work at home but I wasnt sure if it would.

Wednesday, May 18 (at home) 4 hours

To implement my plan, I needed to alter all of the base code starting from the initialization of the grid to the key movement and the random tile genration. At first I tried to create another 2D array to represent the tiles' true locations but it quickly got extremly confusing. So instead I added positon attributes to the tile class to do the job. In the GameWorld class I also made a getTile method that would take row and col values, loop through all the tiles in the grid, and return the tile at respective position. I decided to only focus on the left key movement for now. First I replaced every place that accessed at tile from the tiles array with the getTile method. Then in the tile class I added dx and dy attributes and made the tile move by them in the act method. I also created a setMovement method that could set the tile's dx and dy. Finally in the key movement I made the tile move in its direction by setting its dx and dy attributes and starting the timer. I also set the distance the tile should move so that I could figure out when to stop the timer. After I got this working, I decided to stop here since the process took a while. At this point I hadn't even touched the combining code. 

Frday, May 20 (in class) 1 hour 30 min

In class we realized there was a jumping tile issue where the tile would move smoothly for some time and then jump to its location. We figured this might have to do with the fact I was starting and stopping the timer as well as some other issue in the code I wrote yesterday. So we managed to fix this issue by setting dx and dy to 0 at the end of the movement instead of stopping the timer. We also changed some code in the key movement within the for loop since we realized that everything in the loop would run in an instant - not over a period of time. At this point we got the move code working with animation and needed to start the combine code. We did all the work on my laptop.

Tuesday, May 24 (in class) 1 hour 30 min

Now we actually started on the combine code. We again realized that we would need to change some of the base code since we had to generate new tiles and add them to the array while removing old ones. But this would not be possible in an array. So we did 2 things. First we changed the array to an arraylist that would store the tiles currently in the grid. Second, we made blank tiles part of the background so that they weren't actually a type of tile. Underneath every real tile there would be a blank tile. This made everything a lot easier since we wouldn't have to keep generating blank tiles every time the tiles had to move. At the end of class we sucessfully got key movement to work for the left key. This code was done on Rajvi's laptop.

Tuesday, May 24 (at home) 2 hours

At home I applied the key movement to all 4 keys. Now it looked like the game was working. There were many small errors that I fixed with the animation. I also worked on changing the order that combining occred and the values of tiles were altered. I noticed that the tripple combine error had returned but I decided to leave it be for the time being.

Thursday, May 26 (in class) 1 hour 30 min

Today Allison was excited to work on the GUI and make the game look better. On her laptop, we moved the tiles over and increased the background image, added a new game and how to play button as well as a title and score display, and we changed the fonts and colors of everything. Now the game looked great. At the end of class we realized that the buttons on the top were altering the key movement which would stop our game from working properly.

Friday, May 27 (at home) 1 hour

Rajvi figured out how to fix the key movment and buttons issue. After that, I mamaged the fix the tripple combine error as well as a couple other problems in our code that I hadn't noticed before. Allison did the game over and game won popups and created the instructions display.
 
Saturday, May 28 (at home) 1 hour

To finish the game, I wrote the code to make the new game button work so that it would reset the game when it was pressed. I also used the Score class to update the score display every time a new tile was created. With this our game was officially finished. I pushed the code to the local branch as well as the main branch.
