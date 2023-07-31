---
layout: post
title: Mr. Adam Clock, please report to the ticket counter.
categories:
  - teaching
  - relativity
  - atomic clocks
abstract: >-
  I'm still amazed that we can measure relativity in such a simple way as putting clocks on airplanes.
date: 2018-05-11
---

*Editted 2018-05-11 to fix sign error in the gravitational redshift. D'oh!*

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

The gravitational redshift says that our clock's time measurement will be proportional to its change in energy, so

$$ 
\begin{aligned}
t'/t &= E'/E \\
t' &= t \frac{E'}{E} = t \left( 1 - \frac{GM}{c^2r}\right).
\end{aligned}
$$

Because *t'* > *t*, our clock runs slower near Earth than in deep space.  We could have included kinetic energy into *E'* also, adding time dilation to our equation.  Then the combined clock shift is

$$ t = t' \left( \frac{1}{\sqrt{1-(v/c)^2}}\right)/\left(1 - \frac{GM}{c^2r}\right). \tag{1} $$

## The experiment ##
The original experiment by Hafele and Keating was simple enough: put atomic clocks on airplanes and fly them around the world, and then compare their times with a stationary clock on the ground.
A typical commerical airplane at the time was the [Boeing 707](http://en.wikipedia.org/wiki/Boeing_707), which had a cruising airspeed of *v* = 977 km/hr = 271 m/s.
A typical altitude for a transcontinental flight might be something like *h* = 12,000 m above sea level.

For the actual experiment Hafele and Keating got the flight logs from the flights and used these to estimate the velocity and height of the airplanes along their entire trajectory.  Let's simplify things a bit so that we can do a quicker calculation.  Our airplanes will depart from [Mariscal Sucre International Airport](http://en.wikipedia.org/wiki/Mariscal_Sucre_International Airport) (UIO), which is outside of Quito, Ecuador, just south of the Equator.  We'll place one clock there, which we'll call "L" for "Land clock."
At midnight, two airplanes will take off, one flying due East with a groundspeed of 270 m/s (as measured by a land-based observer) and the other flying due West with a groundspeed of 270 m/s.  Let's name the clock aboard these planes "E" and "W."  We'll assume the planes never need to stop for fuel (mid-air refueling?) until they go completely around the globe and return to Quito.

The Earth's circumference is almost exactly 40,000 km ([Thanks, Napoleon!](http://en.wikipedia.org/wiki/History_of_the_metric_system)), so clock L will record a time for the flights of

$$
t_L = \frac{4\times 10^7\,\mathrm{m}}{271\,\mathrm{m/s}} = 147601.47601476\,\mathrm{s} \approx 41\,\textrm{hours}.
$$

Nothing interesting there.  However, to calculate the time recorded by the airplane clocks, we have to use Eq. (1) above. But, *not so fast!*, the time *t* in the equation is for a clock that is not moving and not affected by gravity.  Our land clock L does experience gravity, and it is also moving as the Earth rotates, so *t* &ne; *t<sub>L</sub>*.  To do the calculation, we need to imagine another clock, that I'll call "S" for "Space clock" that is stationary and far away from gravity, say half way between the sun and [Alpha Centauri](http://en.wikipedia.org/wiki/Alpha_Centauri).

To use Eq. (1), we identify *t* = *t<sub>S</sub>* and *t'* = *t<sub>L</sub>*.  So, our imaginary astronaut reading clock S will say that the airplane flights took a time of 

$$
t_S = t_L \left( \frac{1}{\sqrt{1-(v/c)^2}}\right)/\left(1 - \frac{GM}{c^2r}\right).
$$

We need to put in the values of the variables.  Here's a quick summary, plus a few values we'll need later for the airplanes:

| Symbol | Definition | Value |
|---|---|---|
| *r* | radius of Earth | 40,000 km / 2&pi; |
| *GM* | Newton's constant times mass of Earth[^3] | 3.986 &times; 10<sup>14</sup> m<sup>3</sup>/s<sup>2</sup> |
| *c* | speed of light | 2.99792458 &times; 10<sup>8</sup> m/s |
| *v<sub>L</sub>* | speed of Land clock | $$\frac{40,000\,\mathrm{km}}{1\,\textrm{day}} = 463 \mathrm{m/s} $$ |
|---
| *h* | altitude of airplanes | 12,000 m |
| *v<sub>E</sub>* | speed of East-bound airplane | *v<sub>L</sub>* + 271 m/s = 734 m/s |
| *v<sub>W</sub>* | speed of West-bound airplane | *v<sub>L</sub>* - 271 m/s = 192 m/s |

Ok, so now we can get a number for the time of the flight measured by the Space clock.  Substituting above, we get
*t<sub>S</sub>* = 147601.476117763.  So, the time difference between clock S and clock L is *t<sub>S</sub>*-*t<sub>L</sub>* = 0.000103003 s = 103.003 &mu;s.

::: {.callout-note appearance="minimal"}
That's a lot of digits in the clock times.  We need them because we need to subtract two large numbers that are almost the same.  A cleaner approach is to use Taylor series approximations of the equations using the facts that \|*v*\| \<\< *c* and *h* \<\< *r*.  Then the subtraction mostly cancels algebraically, leaving only the interesting parts.
:::

Now, we use the same formula to calculate the airplane clock times, replacing the "L" variables with the "E" or "W" variables.  The E and W clocks read

$$
\begin{aligned}
t_E &= 147601.476014494\,\mathrm{s}; \\
t_W &= 147601.476014906\,\mathrm{s}.
\end{aligned}
$$

So, finally, the differences between the Land clock and the airplanes clocks are

*t<sub>L</sub>* - *t<sub>E</sub>* = 0.000000266 s  = 266 ns and
*t<sub>L</sub>* - *t<sub>W</sub>* = -0.000000146 s = -146 ns.

This is a tiny amount!  After a voyage of 40 hours, the clocks shift by billionths of a second.  That works out to less than a part in 10<sup>12</sup> error per second in the clocks.  Luckily, portable atomic clocks at the time had a stability of about a part in 10<sup>14</sup>, so the experiment was just within the capabilities of the technology.  (The uncertainty in the planes' trajectories was a larger source of error.)  The actual numbers for the experiment[^1] and their uncertainties are


| Plane | Predicted shift (ns) | Measured shift (ns) |
|---|---|---|
| East | +40 ± 23 | +59 ± 10 |
| West | -275 ± 21 | -273 ± 7 |

The numbers are off compared to our simplified prediction above, but the order of magnitude is correct and the general trend is correct.  Not too bad considering we don't have the original flight data!

## Conclusion ##
I'm still amazed that we can measure relativity in such a simple way as putting clocks on airplanes.  Of course going faster and flying higher will give larger clock shifts relative to a land-based clock.  The [GPS](http://en.wikipedia.org/wiki/Global_Positioning_System) satellites have been serving this function continuously since they first came on line.  Essentially the satellites are just atomic clocks that broadcast their time and position.  The GPS receiver calculates the relative delay of the signal from multiple satellites to solve for its position and time.

One of my favorite GPS stories goes back to the original testing of that system[^4].  The Air Force generals in charge of the program didn't believe the scientists' "voodoo talk" about this relativity stuff, so the original code for the GPS receivers did not include any relativistic corrections.  During the first test, the position numbers started slowly but surely drifting away and the test was considered a failure.  Then one of the engineers dramatically walked over and flipped a switch on the back of the receiver box. Magically everything started working.  He had secretly added the relativity code against orders and rigged up the switch to turn it on, thereby saving the day. Once again the moral of the story is "don't bet against Einstein."


[^1]: J. C. Hafele and R. E. Keating, *Science* 177(4044), 166 (14 July 1972), [doi:10.1126/science.177.4044.166](http://dx.doi.org/10.1126/science.177.4044.166), also [JSTOR:1734834](http://www.jstor.org/stable/1734834).  J. C. Hafele and R. E. Keating, *Science* 177(4044), 168 (14 July 1972), [doi:10.1126/science.177.4044.168](http://dx.doi.org/10.1126/science.177.4044.168), also [JSTOR:1734833](http://www.jstor.org/stable/1734833).
[^2]: A. Einstein, "Zur Elektrodynamik bewegter Körper," *Annalen der Physik* 17, 891 (1905).  An English translation with typos corrected can be found at <http://www.fourmilab.ch/etexts/einstein/specrel/www/>.
[^3]: We can measure the combination *GM* much more precisely than *G* or *M* alone.  (About 10 digits of precision for *GM* compared to 5 for *G* or *M* separately.) It's known as the "[Standard Gravity Parameter](http://en.wikipedia.org/wiki/Standard_gravitational_parameter)."
[^4]: I can't remember the source for this story, which may be apocryphal anyway.  My best guess would be one of Neil Ashby's papers.