---
layout: post
title: Quantum barriers and tunneling, part 1
category: teaching
tags: quantum
excerpt: >-
  I ran into trouble teaching quantum barriers, so here's a different approach (part 1).
---
<!-- kramdown tags defined below -->
{:flt: style="float: right;
       padding-left: 5px;
       padding-right: 0px;
       text-align: center;
       width: 350px;
       box-sizing: border-box;
       "}
<!-- end kramdown -->

My quantum mechanics class did really well last semester, but one topic that tripped up a lot of people on the final exam was a one-dimensional barrier problem.  The potential energy function looks something like

$$ U(x) = \begin{cases} 0 & x \lt 0 \text{ or }x \gt a \\ U_0 & 0 \lt x \lt a \end{cases}. $$

Where \\( U_0 \gt 0 \\) and for now I'll only look at the case when the energy of the particle is \\( E > U_0 \\).

The trouble that the students had is that many of them treated this problem as two steps in series, ignoring the important interference effects.

So, first let me solve the single step problem to show where they are starting from and to introduce notation.
Next, I'll show the _incorrect_ solution and point out what it misses.
Then I'll solve the barrier problem two ways.
First, I solve this the "traditional" way found in most intro quantum books[^1] [^2] that my students had trouble remembering.
I think I also have a diagnosis about why they forgot the solution, which I'll discuss.

Then, in a follow up post, I'll solve the same problem a different way, borrowing from a similar optics problem[^3] [^4] ([dielectric Fabry-Pérot etalon](https://en.wikipedia.org/wiki/Fabry%E2%80%93P%C3%A9rot_interferometer)) and show that you get the same answer, but with, IMHO, the physics being more apparent.

The trade off is in the math.  The first method requires solving four simultaneous linear equations, while the second method uses infinite series. YMMV regarding which is easiest.

## References
[^1]: Griffiths quantum mechanics

[^2]: McIntyre quantum mechanics

[^3]: Hecht optics

[^4]: Pedrotti optics