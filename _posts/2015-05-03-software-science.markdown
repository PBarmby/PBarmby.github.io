---
layout: post
title:  "Software and science"
date:   2015-05-03
tags: science software astronomy
comments: True
---

[No monthly wrap-up for now; other things to talk about..]

At the Python in Astronomy workshop, we had a discussion about career credit for software development,
the notes of which are [here](https://docs.google.com/document/d/1aXOQdM46gAGCJEt1LvF0zFHlq-mtaZ9HOgvOHD7gy00/edit?pli=1).
During the session I fired off a Tweet to [C. Titus Brown](http://ivory.idyll.org/) to ask for ideas. This spawned
a Twitter discussion (which ensued during the face-to-face discussion!). Titus wrote a 
[blog post](http://ivory.idyll.org/blog/2015-software-as-a-primary-product-of-science.html) which spawned 
more interesting discussion, both in the comments and in follow-up posts:

* [Daniel Katz](https://danielskatzblog.wordpress.com/2015/04/22/software-can-be-a-primary-product-of-scientific-research/)
* [C. Titus Brown](http://ivory.idyll.org/blog/2015-more-on-software.html)
* [Kyle Cranmer](http://theoryandpractice.org/2015/05/Software:%20citation%20and%20status/#.VUZr5GZf6RM)
* [Konran Hinsen](https://khinsen.wordpress.com/2015/04/23/software-in-scientific-research/)

A lot of the commentary so far has been from the point of view of biology or particle physics, and I would
argue that observational astrophysics is in a middle ground between these two. We don't have
the everyone-has-their-own equipment like biologists now do we have the everyone-uses-one-big-facility like
particle physics; instead we get our data from a mix of observatories which don't belong exclusively to anyone.
Our data is all digital; we need software to analyze it, much of which is not specific to any one
facility. To avoid duplicating effort, it makes sense to develop a community software library that everyone can use
and contribute to. Of course, one such library is [astropy](http://www.astropy.org), but it's not the only one.

Should the work that goes into developing software-for-science be called science itself? I think
that it's more like engineering, but with the critical difference that *it has to be done by scientists* or at least
people with a deep connection to, or understanding of, the science involved. In astronomy, with its lack of
commercial applications, there's unlikely to ever be an off-the-shelf product that will serve our needs; if
we don't write our own software, no one will do it for us. Writing the code isn't doing science per se, but
it's *enabling* science, in much the same way as building instruments for telescopes is. [I think a different
argument might possibly be made for computational astrophysics, but that's someone else's to make.] Both are an
important part of the research ecosystem. In some ways they function like the "service" part of academia:
necessary for everyone but performed only by some.

So back to what we were discussing at Python in Astronomy: how to credit people for their contributions to software?
 Right before our workshop, 
a [report](https://softwaredatacitation.org/Workshop%20Report/SoftwareDataCitation_workshop_report_2015_April_20_without_logo.pdf) on tthe topic came out; it makes some interesting suggestions but a lot of them focus on citations.
For software, the citation system seems clunky: authors of a paper are fixed, but 
the contributors and maintainers of software can change.
Conference presentations don't seem the right avenue either. One of the
things we talked about during our discussion was how to create metrics for software/contributions; 
[openhub.net](https://www.openhub.net/) seems to have made a start in that direction. 

This is an important discussion that is just getting started. I don't see a lot of it happening in Canada
just yet (maybe I'm not looking in the right places?) I suspect we will probably end up doing what we 
usually do and following the bigger players, but I think we better pay attention. We can do better research
and learn more about the world if we're not all reinventing the wheel, and we need to work out how best
to reward people who make the wheels better.

