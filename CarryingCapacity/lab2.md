#Carrying Capacity
Carrying capacity is the maximum size population a given environment can support. For example, if a field is inhabited by grass and grass-eating rabbits. Then what is the maximum rabbit population? The answer depends on the rate rabbits eat and mate as well as the rate that grass grows. If grass grows back quickly, then the population growth for rabbits will be exponential. Otherwise we should see something like the familiar S-curve of logistical growth. The horizontal asymptote is the carrying capacity of the environment:



This lab customizes the Eco-0 Framework.

Patches and turtles have 0 to 100 units of stored energy:

```
patches-own [penergy]
turtles-own [energy]
```
Here are the patch and turtle update procedures:
```
to update-patch
  let luck random 100
  if penergy < 100 and luck < growing-probability
  [
    set penergy penergy + 1
  ]
  set pcolor scale-color green penergy -50 150
end

to update-turtle
  eat
  mate
  move
  if energy <= 0 [die]
end
```

Notice how the growing-probability is used to control the grow-back rate for grass.

* If a rabbit has at least 10 units of energy, it moves a few steps in a random direction. This consumes 10 units of energy.

* If a rabbit needs energy, and if it is lucky, it takes as much energy as it needs or is available from the patch it occupies (use patch-here).

* If a rabbit has at least 60 units of energy and is lucky, then it can hatch a single rabbit. This consumes 20 units of energy.