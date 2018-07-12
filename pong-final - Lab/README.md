The point of this initial lab was to add horizontal paddles to Pong. Since the entire game was already created in Lua for this lab,
the implementation involved more about understanding the current program than a need to problem solve. The important additions made
were adding a variable within the Paddle class that keeps track of the paddle's x velocity, then in main, paddles 1b and 2b are defined
and rendered with flipped proportions of the current paddles. 
The latter - 2b - had some issues where it kept rendering offscreen, which through some trial and error, I realized was due to the
coordinate I'd set it to being too far, despite that placement being a flipped version of paddle 2's.
Once those were rendered properly to the screen, the ability to move each player's designated horizontal paddle was added, plus
a check to ensure that the paddles couldn't go offscreen horizontally, similar to how the other paddles were already restricted to the 
screen's height vertically.
With that done, all that needed to be added was to have the ball react properly when colliding with the new paddles, and to update the
paddles each dt.
