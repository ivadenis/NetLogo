Turtles (bugs) have rhythm:

    turtles-own [ rhythm ]

Initially, the rhythm of a turtle is random.

    to init-turtle
        setxy random-xcor random-ycor ; send each turtle to a random position, for example
        set rhythm 1 + random 10
        set color gray
        set shape "bug"
    end

In every update cycle a turtle turns off his flash, moves randomly, turns on his yellow flash if ticks is divisible by rhythm, then updates his rhythm to be the most popular rhythm of his neighbors:

    to update-turtle
        set color gray
        move
        flash
        update-rhythm
    end

We can use the modes function to get a list of the most popular rhythms among nearby turtles:

    set rhythm one-of modes [rhythm] of nearby-turtles


