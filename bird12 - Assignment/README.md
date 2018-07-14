Starting with a recreation of Flappy Bird made in Lua, several aspects of the game were asked to be changed. The gap between pipes went
from a static number to a random number, same with the interval of time between pipes spawning. A medal is awarded based on the player's
ending score each run, and an added pause feature allows the user to suspend and resume the game as they please. Also fixed a bug where
the player could go above the screen's height unintentionally by capping their y location.

The pause feature was surprisingly tricky to impliment, though it may have felt that way since the ability to register the player hitting
'enter' also needs to recognize if the player hits 'return', as keyboards can use either or. Took a minute to figure that out. After that
hiccup, I created a variable within the player's own class that keeps track of whether or not they've paused the game, suspending their
gravity and saving their velocity so that when unpaused, they wouldn't have collected any extra velocity and immediately plummet.

Could've probably made it a lot easier on myself by doing all those changes within the PlayState state, but the opportunity went over
my head in trying to figure out why hitting enter wouldn't work. Can't say I'm all too bothered by it being a lil' backwards though.
