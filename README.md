# Project: Melting an Icy Moon
McGill Physics Hackathon 2023


Jesse Sutherland and Susan Zhou

Below is the project description as submitted on the [devpost](https://devpost.com/software/melting-an-icy-moon).

## Inspiration
When we read the Quanta magazine article "These Moons Are Dark and Frozen. So How Can They Have Oceans?" we were fascinated by the possibility of liquid oceans on the icy moons of Jupiter and Saturn, and the implications it would have for extraterrestrial life. From a search on wikipedia, we found that an equation exists that calculates the heating rate due to tidal friction, which depends on the orbit parameters and the Love number, which is specific to the moon and describes how well the heating due to tidal friction permeates through the moon. We became interested in the melting process due to this fixed heating rate.

## What it does
We created a hypothetical scenario of a moon covered in a 100-km-thick layer of ice, using sample data inspired from Jupiter's moon Europa. We calculate the progression over time of the melting of this layer of ice, assuming a constant heating rate coming from the inside of the moon, calculated using the equation found online.

## How we built it
We made the simplifying assumption that the melting occurs layer by layer. We used the equation delta_Q = C_p*delta_T, where C_p is the heat capacity of the substance, delta T is the temperature change required to reach melting point, and delta_Q is the heat input in a fixed time interval. This allowed us to iterate over each layer, and find the time required to melt it.

## Challenges we ran into
We realized there are a number of changing parameters involved in this process. For example, as the ice melts, the pressure exerted on the lowest layer of ice will decrease, and thus the heat capacity C_p, which is both pressure and temperature dependent, will change.

We also realized that in reality, the heating wouldn't exclusively melt one layer before moving on to the next, but would progress continuously throughout all layers. We attempted to simulate this process using Fourier's law of heat conduction, but our code ran into bugs.

## Accomplishments that we're proud of
Thinking about and attempting to solve a multi-factor physics problem by considering different scenarios and assumptions.

## What we learned
Using Github, How to animate matplotlib plots using moviepy library.

## What's next for Melting an Icy Moon
Improve our model to make it more realistic, and consider other aspects of the problem, such as simulating orbits to calculate the tidal heating.

