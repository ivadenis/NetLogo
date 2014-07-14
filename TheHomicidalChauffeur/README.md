The Homicidal Chauffeur
Imagine it's late at night. You are on foot and must cross a vast empty parking lot. Suddenly, from the shadows you hear a car engine start. Lights come on. Tires squeal. The car speeds toward you. You can turn faster but he can move faster. Can you survive?

Let's build a computer simulation to find out. In this simulation a blue turtle represents the pedestrian and a red turtle represents the car. Sliders allow us to adjust the speeds of the car and pedestrian as well as the turning radius of the car. A switch allows users to turn on and off the path tracing feature. If and when the car hits the pedestrian, we hear a beep and the simulation ends.

Here's a screen shot if the interface:



Initially, the two turtles are 20 steps apart.

On each update cycle, the pedestrian faces the car, randomly turns 90 degrees to the right or left, and runs the maximum number of steps allowed by his speed.

The car turns toward the pedestrian as far as it can, then drives the maximum number of steps allowed by its speed.

When the pedestrian is near the edge of the parking lot, he turns 180 degrees and runs.

When the car is near the edge of the square parking lot, it backs up the maximum number of steps allowed by its speed.

Note: You may assume wrapping is turned off in the system settings dialog. Ignore the wrap on-off button in the screen shot.

Hints

Recall that zero degrees is north (i.e., the top of the screen), 90 degrees is east, etc.

We can set the heading of a turtle using the set (assignment) command:

set heading

or by turning the turtle right or left some specified number of degrees:

rt 90
lt 30

NetLogo provides some useful procedures for computing headings:

can-move n              ; = false if wrapping off and agent can't move forward n steps without hitting edge

towards agent           ; = heading towards agent

towardsxy x y           ; = heading toward the point (x, y)

face agent              ; set heading towards agent

facexy x y              ; set heading towardsxy x y

subtract-headings x y   ; = z where y + z = x or y – z = x

Suppose the car's heading is 70 degrees. Suppose the heading in the direction of the pedestrian is 50 degrees. Then the car should turn left turning-radius degrees.

After the turn is made, the car should advance. Be careful not to overshoot the pedestrian.

Behavior Space

Behavior Space is a NetLogo tool that allows you to automate many runs of the model and collect the data in a spread sheet. In each experiment you can specify settings of the sliders and other model parameters. Use this feature to determine how often the car gets the pedestrian given a variety of settings for car speed, pedestrian speed, and turning radius.

Making Movies

You can generate a QuickTime movie of your simulation by executing the movie-start command at the beginning of a simulation, the movie-close command at the end of the simulation, and the movie-grab-view command each time the movie is updated.

 

 


