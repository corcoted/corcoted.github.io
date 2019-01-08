---
layout: post
title: Geometric Algebra - beyond vectors
category: math
tags: reading
excerpt: >-
  I stumbled onto the topic of Geometric Algebra (Clifford Algebra) a while back.  Does it help us understand physics?
---

I read a lot.  It's probably my biggest hobby.  I like to mix nonfiction and fiction, and I include work-related things that aren't directly tied to my current teaching or research.  This post falls into the last category.

The theme I've been riding recently is things that aren't taught to physicists but maybe should be.  These are actual physics topics or physics-tangent topics that I know next to nothing about and didn't really even hear about until recently.  (I also have a list of non-physics things that I think physicists tend to lack, but that's a rant for another day.)  I am a rank novice in the topic below, so please forgive any errors.  I'll post more on these if I gain any shareable insights.

## Geometric Algebra
The math we learned as undergraduates to describe the physical world is broken.  Since Gibbs introduced vectors in the late 19th century and silenced Hamilton's [quaternions](https://en.wikipedia.org/wiki/Quaternion), justly or unjustly, we've made them a cornerstone of physics, but they become awkward when we start to talk about rotations or magnetic fields, for example, because we begin trying to paste vectors onto objects that aren't just "a magnitude plus a direction."  For example, where the heck does the right-hand rule for cross products come from?  It's so bizarre and artificial when you think about it.  In the end it traces back to us deciding that *x*, *y*, and *z* should be related to each other in some particular way and we need everything else we do to be consistent with that.

[Geometric Algebra](https://en.wikipedia.org/wiki/Geometric_algebra) comes from W. K. Clifford's work in the late 1890's to build up higher dimensional objects from products of vectors without throwing away information.  What I mean by this is that the two vector products that we learn, the dot product and the cross product, both throw something away -- in some ways they complement each other.  Clifford combined the two into a "geometric product" to build areas and volumes out of vectors in a seemless way.

I first saw this a few years ago when my colleague [Michael Huster](https://www.duq.edu/academics/faculty/michael-huster) lent me his copy of [Alan McDonald's *Linear and Geometric Algebra*](http://www.faculty.luther.edu/~macdonal/laga/) which gives an introduction to the topic from a math point of view.  I admit that my initial take was that geometric algebra was just some book-keeping trick and not really that useful.  In my defense, a lot of the research papers on the topic use GA in just that way, as a superficial compactification of notation.

I stumbled back onto the topic during my prep for teaching Electrodynamics last year, and started reading through some of [David Hestenes'](https://en.wikipedia.org/wiki/David_Hestenes) papers.  I guess what hooked me back in was this nagging feeling that the math we use, particularly vector calculus, is an impediment to understanding the physics that it describes.  My students always struggle to apply Maxwell's Equations to problems and I sympathize with them.  I realize that the only reason I can navigate the topic is that I've memorized a bunch of tricks and informal rules but that I don't have truly deep intuition beyond what experience tells me is the right way to solve problems.  I think that by better understanding the structure of geometry (whether or not geometric algebra is the right tool for that), I might gain some insight into how the universe is constructed.

The book [*Geometric Algebra for Physicists* by Chris Doran and Anthony Lasenby](http://www.mrao.cam.ac.uk/~cjld1/pages/book.htm) [^1] is a good overview written from a physics perspective.
It seems like Electrodynamics is one of the topics where this has the biggest impact.
For example, all of Maxwell's Equations can be reduced to a single equation in this system.


So, here's what bugs me about all of this.  All of this stuff is old news to mathematicians.  It just hasn't trickled down from the etherial heights of pure rational thought to us ground dwellers on the material plane.  I bailed on the pure math classes as an undergrad (a bad "Intro to proofs" professor ruined it for me), so I can only blame myself that I can't parse the jargon and writing style of math literature, but I wish there were more accessible resources for learning higher math.  This book is a small crack in the wall to help me think about these things.

Oh, and I now think [conformal geometry](https://en.wikipedia.org/wiki/Conformal_geometry) is cool and can probably solve some nagging questions that have been in my head for a while about the shape of [gaussian laser beams](https://en.wikipedia.org/wiki/Gaussian_beam).  If I figure it out, I'll be sure to pass it on.

[^1]: Chris Doran and Antony Lasenby. *Geometric Algebra for Physicists*, Cambridge, 2007. ISBN: 9780521715959 