# Spread of Memes
A meme is a fashion, idea, joke, or other bit of cultural flotsam that is spread from one agent to another through some form of social contact. Memes spread like viruses, but they tend to fade and can have different strengths in different agents. For example, if a joke is funny, then it fades from memory more slowly.

In this project our aim is to determine how long a meme can survive in a social network. Sliders allow users to control the fade-rate of a meme and the initial percentage of the population infected by the meme:



Each turtle has a meme enthusiasm property, which is a number between 0 and 100 that determines how enthusiastic the turtle is about some meme. A graph plots the mean enthusiasm of all turtles. Initially, only a percentage of the population—determined by the infection-rate slider—has any enthusiasm at all for the meme. (Say between 50 and 100.)

When a turtle is updates, it selects a neighbor within radius 5. If that neighbor's enthusiasm is less than the executing turtle, then the neighbor's enthusiasm is set to the sum of the enthusiasms of the two turtles (or 100, whichever is smaller.) The idea being that the neighbor's enthusiasm is augmented by the enthusiasm of a more enthusiastic turtle. (Feel free to explore other infection formulas.)

The executing turtle then decrements its enthusiasm by some random amount less than fade-rate, and it moves randomly. The color of a turtle should be shaded by its enthusiasm.

 