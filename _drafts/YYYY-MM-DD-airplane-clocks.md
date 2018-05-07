---
layout: post
title: Mr. Adam Clock, please report to the ticket counter.
category: teaching
tags: relativity, atomic clocks
excerpt: >-
  Brief summary or excerpt of the post.
---

Last week I gave a homework problem on one of my favorite experiments testing relativity: flying atomic clocks around the world on commercial airplanes to measure time dilation.
The original experiment was published in *Science* 1972 by Hafele and Keating[^1].
The experiment tests two aspects of Einstein's relativity: moving clocks move slower (time dilation) and clocks in gravity move slower (gravitational redshift).

## Background ##
### Time dilation ###
Time dilation can be stated simply as "moving clocks are slower than stationary clocks."  In Einstein's first paper on Special Relativity[^2], he gives a nice derivation of this using a thought experiment with a moving train.  If I call the time measured on the stationary clock as *t* and the moving clock as *t'*, the two values are related by

$$  t = \frac{1}{\sqrt{1-(v/c)^2}}\,t' $$

where *v* is the speed of the moving clock, as measured by the stationary clock, and *c* is the speed of light.  The factor out in front of *t'* appears often enough that we'll give it a new name, *&gamma;*.  One important prediction of relativity is that no massive object can move faster than light, so *v* < *c*, making *&gamma;* > 1 and, therefore, *t* > *t'*.  So, the stationary clock records a longer time interval than the moving clock.  Or, as we said before "moving clocks are slower."

### Gravitational redshift ###
This one is a bit tricker and not really discussed in undergraduate courses.  To really get to the meat of General Relativity we have to talk about geometry and curved spacetime.  That's deeper that I want to go in this post, but a good way to think about this is that, to a first approximation, a clock in a gravitational field will slow down proportional to its change in potential energy.

For example, a clock with mass *m* at rest in empty space has an energy of *E* = *mc*<sup>2</sup>.  (You already knew that, right?)
If we put this clock near a massive object (like the Earth) with mass *M*, we add the potential energy of gravity to the energy.  For things less massive than black holes, we can just use the Newtonian gravitational energy, so the total energy of a clock at rest near Earth is

$$ E' = mc^2 - \frac{GMm}{r} $$

where *G* is Newton's gravity constant and *r* is the distance from the center of the Earth to our clock.

The gravitational redshift says that our clock's time measurement will be inversely proportional to its change in energy, so

$$ 
\begin{aligned}
E't' &= Et \\
t &= t' \frac{E'}{E} = t' \left( 1 - \frac{GM}{c^2r}\right).
\end{aligned}
$$

Because *t'* > *t*, our clock runs slower near Earth than in deep space.  We could have included kinetic energy into *E'* also, adding time dilation to our equation.  Then the combined clock shift is

$$ t = t' \left( \frac{1}{\sqrt{1-(v/c)^2}} - \frac{GM}{c^2r}\right). $$

## The experiment ##
The original experiment by Hafele and Keating was simple enough: put atomic clocks on airplanes and fly them around the world, and then compare their times with a stationary clock on the ground.
A typical commerical airplane at the time was the [Boeing 707](http://en.wikipedia.org/wiki/Boeing_707), which had a cruising airspeed of *v* = 977 km/hr = 271 m/s.
A typical altitude for a transcontinental flight might be something like *h* = 12,000 m above sea level.

For the actual experiment Hafele and Keating got the flight logs from the flights and used these to estimate the velocity and height of the airplanes along their entire trajectory.  Let's simplify things a bit so that we can do a quicker calculation.  Our airplanes will depart from [Mariscal Sucre International Airport](http://en.wikipedia.org/wiki/Mariscal_Sucre_International Airport) (UIO), which is outside of Quito, Ecuador, just south of the Equator at a elevation of 2,400 m above sea level.  We'll place one clock there, which we'll call "L" for "Land clock."
At midnight, two airplanes will take off, one flying due East with a groundspeed of 270 m/s (as measured by a land-based observer) and the other flying due West with a groundspeed of 270 m/s.  Let's name the clock aboard these planes "E" and "W."  We'll assume the planes never need to stop for fuel (mid-air refueling?) until they go completely around the globe and return to Quito.

The Earth's circumference is almost exactly 40,000 km ([Thanks, Napoleon!](http://en.wikipedia.org/wiki/History_of_the_metric_system)), so clock L will record a time for the flights of

$$
t_L = \frac{4\times 10^7\,\mathrm{m}}{271\,\mathrm{m/s}} = 147601.476015\,\mathrm{s} \approx 41\,\textrm{hours}.
$$

#### Footnotes ####
[^1]: J. C. Hafele and R. E. Keating, *Science* 177(4044), 166 (14 July 1972), [doi:10.1126/science.177.4044.166](http://dx.doi.org/10.1126/science.177.4044.166), also [JSTOR:1734834](http://www.jstor.org/stable/1734834).  J. C. Hafele and R. E. Keating, *Science* 177(4044), 168 (14 July 1972), [doi:10.1126/science.177.4044.168](http://dx.doi.org/10.1126/science.177.4044.168), also [JSTOR:1734833](http://www.jstor.org/stable/1734833).
[^2]: A. Einstein, "Zur Elektrodynamik bewegter Körper," *Annalen der Physik* 17, 891 (1905).  An English translation with typos corrected can be found at <http://www.fourmilab.ch/etexts/einstein/specrel/www/>.