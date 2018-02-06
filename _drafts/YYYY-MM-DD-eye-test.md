---
layout: post
title: Simple eye test
category: teaching
tags: optics
---
Most of us are familiar with the "refraction" exam done by optometrists to determine our eyeglass prescription.  The test involves the patient trying to read a chart placed at reading distance (10 in = 25 cm) or a standard far distance (20 ft = 6 m) while the optometrist tries placing different lenses in front of each eye to find the lens that gives the best image for the patient.
The test is largely trial-and-error.  A good practicioner can reach an optimal lens with only a few trials, but there's a more direct method to measure myopia (nearsightedness), hyperopoia (farsightedness), and presbyopia (age-related farsightedness).  The only tool we need is a tape measure and an object to look at.  (Unfortunately this test doesn't work for astigmatism, the other common vision defect.)

### Normal vision
"Normal vision" means that a person can clearly see an object at both reading distance (25 cm) and at far distance (infinity).[^1]  We can model this as a single lens with variable focal length *f* and a fixed image distance *s'*.  A good approximation is that *s'* = 16.7 mm.[^2]  Using Gauss's Lens equation we can solve for the values of focal length in the near and far cases:

$$
\begin{align*}
\frac{1}{f} &= \frac{1}{s} + \frac{1}{s'} \\
f_{far} &= \left(\frac{1}{\infty} + \frac{1}{16.7\,\mathrm{mm}} \right)^{-1} = 16.7\,\mathrm{mm} \\
f_{near} &= \left(\frac{1}{250\,\mathrm{mm}} + \frac{1}{16.7\,\mathrm{mm}} \right)^{-1} = 15.7\,\mathrm{mm} 
\end{align*}
$$

The ability of the human eye to change its focal length is called *accomodation*.  As we age we lose this ability and the eye gets stuck more towards the *f<sub>far</sub>* value.  This is why older people need reading glasses.  It's also why the medicine used to dilate pupils for an eye exam make it difficult to read: the muscles responsible for accomodation are paralyzed so the lens is stuck in "far" mode until the medicine wears off.

> Did you ever wonder why eye exams are done in a darkened room?  This is to dilate the pupils and *maximize* the effects of aberations in the eye's optical system.  This makes the test more sensitive.  One side effect is that spherical aberation makes the effective focal length of the eye shorter than it would be in bright light -- this effect causes night-time myopia.

So, just to recap: a normal, healthy eye can vary its focal length between *f<sub>far</sub>* = 16.7 mm and *f<sub>near</sub>* = 15.7 mm.

### Optical power and diopters
Optometrists don't speak in terms of focal length but in terms of optical power.  Optical power is defined as the reciprocal of focal length:

$$
P = \frac{1}{f}
$$

and is usually specified with units of "diopters" = m<sup>-1</sup>.  So, we can express the focal length range of the eye in terms of optical power instead:

$$
\begin{align*}
P_{near} &= \frac{1}{f_{near}} = \frac{1}{15.7\,\mathrm{mm}} = 63.9\,\mathrm{m^{-1}} = 63.9\,\text{diopters} \\
P_{far} &= \frac{1}{f_{far}} = \frac{1}{16.7\,\mathrm{mm}} = 59.9\,\mathrm{m^{-1}} = 59.9\,\text{diopters} 
\end{align*}
$$

### Eyeglasses

Diopters are also the units used for eyeglass and contact-lens prescriptions.  If your eyeglasses are *P* = -5.00 diopters, then they
have a focal length of *f* = 1/*P* = -0.2 m.

So, what do eyeglasses do?  In the approximation that the lenses are close to the eye, the optical power of the eyeglasses adds to the optical power of the eye's lens.

### The test
The test is simple.  Take a tape measure and stretch it out as far as possible (on the floor of a hallway works best).  With your eye placed at the end of the tape measure, move an object as close as possible such that you can still clearly see it.  Record this distance as *d<sub>near</sub>*.  Next, move the object as far away as possible along the tape measure until it is just no longer clear.  Record this distance as *d<sub>far</sub>*.  (If you can place the object all of the way at the end of the tape, let *d<sub>far</sub>* = &infin;.)  If *d<sub>far</sub>* &ge; 6 m and *d<sub>near</sub>* &le; 25 cm, then you have "normal" vision.  If your measurements aren't in those limits, then we can do a little algebra to calculate an eyeglass prescription.

TODO -- write up the calculation.

### References
[^1]: Pedrotti

[^2]: In an actual human eye the interior is filled with *vitreous humor*, a gel substance with an index of refraction of about *n* = 1.33.  For simplicity, I've adjusted the actual image distance (approximately the diameter of the eye = 22 mm) to account for the index of refraction.  The focal lengths I use above are the object-side focal lengths.
