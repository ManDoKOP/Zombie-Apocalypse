We have seen that Monte Carlo simulations can be very useful for modelling complex situations, often in the real world.  Examples of this include the predator/prey model that is designed to simulation populations of wildlife.    Recently the BBC ran a program modelling the effect of a flu pandemic in the UK which used a Monte Carlo simulation:

https://www.bbc.co.uk/programmes/p059y0p1 Contagion! The BBC Four Pandemic

However, as we have been hearing about zombie outbreaks during the intensive week, for this assignment you are asked to model an outbreak of zombies.    I’ve included a paper on the maths of modelling such an outbreak that shows the factors for the model and how it can be solved mathematically.   This web page : http://scipy-cookbook.readthedocs.io/items/Zombie_Apocalypse_ODEINT.html gives the equation as:

dS/dt = P - BSZ - dS dZ/dt = BSZ + GR - ASZ dR/dt = dS + ASZ - GR

with the following factors:
•	S: the number of susceptible victims
•	Z: the number of zombies
•	R: the number of people "killed"
•	P: the population birth rate
•	d: the chance of a natural death
•	B: the chance the "zombie disease" is transmitted (an alive person becomes a zombie)
•	G: the chance a dead person is resurrected into a zombie
•	A: the chance a zombie is totally destroyed

This page shows how to use Python to solve this equation as an ordinary differential equation.  However, while this solves the equation over time, it does not give us an idea of how fast the zombies will travel.  So we need to add a new factor:

•	V: Speed of a zombie.
And possibly
•	v: Speed of a non-infected person.

Now we have added that factor the equation can not be solved as easily.  This can be modelled by a random walk simulation, with the first set of factors controlling the population and the chance of a victim.  You might like to set up the model with geographically separated non infected populations and investigate how the infection spreads. 

For this assignment write a model in R or Python (or both if you think it help) to model a Zombie outbreak with geographically separated populations.  Show how the factors above effect the speed of the outbreak.  
