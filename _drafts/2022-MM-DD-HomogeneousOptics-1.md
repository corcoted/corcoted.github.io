---
layout: post
title: Optics in Homogeneous Coordinates, Part 1
category: research
tags: optics
excerpt: >-
  I introduce the homogeneous representation of rays and extend the ABCD matrices to include rotations and translations (properly!).
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

<!-- 
Reminder that mathjax is enabled.  Inline math using double backslash parenthesis: \\( \\) 
Display math using double dollar or double backslash bracket: $$ $$ or \\[ \\]
-->

<!--
kramdown reference: https://kramdown.gettalong.org/quickref.html
-->

*This is the first post discussing my upcoming paper on a new way to look at geometric optics.  I'll add the link to the paper itself once it reaches press.  These blog posts will focus on how to use the results.*

## Motivation

### Case 1: Imaging problems

When teaching undergraduate optics, I always found the problems containing series of lenses and mirrors tedious.  The standard solution is to find the image of an object created by each optical element using Gauss's Lens equation.  This image then becomes the object for the next element.  Apply Gauss's equation again. Rinse and repeat.  For one or two lenses this is not too bad, but once you get to something like a microscope (objective, tube lens, and ocular), then it really drags.  Worse, if your object moves a little bit you have to start over.  And there is also the weird issue of infinitely far objects and images to deal with.  It seems a little incomplete.

### Case 2: Ray tracing

In my research lab, we mostly deal with lasers, which to a reasonable approximation can be treated as geometric rays (at least as far as alignment is concerned).
When sketching out a new optical setup, I'll often use [Ray transfer matrices](https://en.wikipedia.org/wiki/Ray_transfer_matrix_analysis) (also called "ABCD" matrices) to set things up.  Each ray is represented as a vector containing the ray height and slope.  Each optical element corresponds to a matrix.  By multiplying these matrices together we can get a representation of the entire optical system.  Matrix times input ray equals output ray.

*But wait! There's more!*
The same ABCD matrix that describes the path of geometric rays through the system also describes the change in size of Gaussian laser beams as they travel through the system.  This seems like magic, because there is no apparent relationship between rays and the size of diffracting laser beams.  The detailed proof requires digging into the nuts and bolts of the diffraction integrals.  Surely there is a simpler explanation.  (Arnaud has a partial explanation using [complex-valued rays](), which again seems like magic, but at least understandable magic.)

### The goal: Unifying the ray and image paradigms

What I would really like to do is find a solution to imaging problems that is as simple to use as the ABCD matrices.  One solution is that I can build two rays that pass through my object point and find where they intersect on the output side to locate the image, but that's still a lot of algebra, and I am lazy.  Can I get there more directly?

The answer is "yes," but first I need to re-examine what the ABCD matrices are doing to the rays, in a geometric sense.