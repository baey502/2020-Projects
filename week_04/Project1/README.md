Ping Pong

This program will demonstrate a simple ping pong game between an user (you) and an opponent (ai).
The objective is to rally without missing any balls and if the ball is missed, 
it will restart from the center to a random direction.
There are two versions of this game, one without functions and one with functions.

First, pygame will be imported and the dimensions of the screen will be set to 800 x 600.
Random will be integrated for the speed of the ball so that it bounces towards a random direction.

While true, the program will check for any user input.
This is put in a while loop so that it will constantly repeat the loop to check for updates. 
It will check if the user closes the window, in that case, quit the program.
It will also check if there is user input for up/down buttons, 
in that case, move the user's paddle up or down by increments of 7.

For the ball to move, the speed of x and y will be set as global variables.
The ball will bounce back when it hits the paddle (colliderect), the top or bottom walls. 
This is determined by the *-1.
However, if it hits either the left or right walls, it will restart from the center towards a random direction.
This is the ball_move function.

The user can move freely within the set parameters of the screen, but cannot go beyond it.
When it goes beyond the top or bottom of the screen, it will place the user on the location of top and bottom, 
so there is no further movement. This is the player_move function.

The opponent(ai) will move accordingly to the ball so the user can bounce the ball back and forth.
If the opponent's top is above the ball, it will move down to hit the ball.
If the opponent's bottom is below the ball, it will move up. 
This is the opponent_move function.

Then, the screen is filled with the background color 'grey12'.
This is drawn first so it begins on the bottom and the rest of the elements are drawn on top of it.
Two rectangles are drawn for the paddles of the user and the opponent.
An ellipse is drawn for the ball and a line is drawn to divide the center of the screen.

Lastly, pygame.display.flip() updates the window and the clock.tick limits how fast the code is run. 