---
layout: post
title: "Data sharing in astronomy, part 2"
date: 2016-02-04
tags: astronomy science data
comments: True
---

Or, "The Virtual Observatory: are we there yet?"

At the end of the [previous post]({% post_url 2016-01-27-Data-sharing-in-astronomy %}), I mentioned that
there is a lot of freely-available astronomy data, but finding it can be a problem. The proposed 
solution to this is an idea called the Virtual Observatory, "the vision that astronomical
datasets and other resources should work as a seamless whole."  So what exactly *is* this Virtual Observatory --
is it a website you can use to download all the data from every telescope ever, on whatever piece of
the sky you care about? Not so much. In fact there is not one virtual observatory but a 
[whole bunch of them](http://www.ivoa.net/about/member-organizations.html) including
[EuroVO](http://www.euro-vo.org/), [Canadian Virtual Observatory](http://www.cadc-ccda.hia-iha.nrc-cnrc.gc.ca/cvo/), [VO-India](http://vo.iucaa.ernet.in/~voi/) and many more. It's not totally clear to me what the
situation in the US is: the [USVAO](http://www.usvao.org) seems to have been succeeded by the [US VOA](https://hea-www.cfa.harvard.edu/USVOA/). Yes, astronomers love our acronyms..

The [International Virtual Observatory Alliance](http://www.ivoa.net/), which has been around for
over 10 years, coordinates the efforts of all of the individual VOs. They have meetings to coordinate on 
standards -- what format should we use for tabular data? How should we query astronomical databases? How
should metadata be described? My impression as someone who doesn't work on VO issues is that the
IVOA involves lots of meetings and [jargon](http://www.ivoa.net/astronomers/vo_glossary.html) but not
always that much action. This is perhaps because a lot of their work goes on under the surface, where
it's not that obvious. Bruce Berriman's blog has a nice summary of [the US VAO's closeout report](https://astrocompute.wordpress.com/2014/08/29/the-impact-of-the-virtual-astronomical-observatory/), which tries to get at the impact
of the US efforts in particular.

The IVOA site lists a whole pile of [VO applications for astronomers](http://www.ivoa.net/astronomers/applications.html).
Many of these are software packages that I use all the time, like [ds9](http://ds9.si.edu/site/Home.html) and 
[TOPCAT](http://www.star.bris.ac.uk/~mbt/topcat/sun253/sun253.html), but 
even though I work with a lot of public astronomy data, I haven't made use of
a lot of the VO search tools listed. (I don't think my students have either, so maybe it's not just
my advanced age. Or maybe they don't use these things because I don't show them how?)
Some of the search tools look pretty cool, and I really should try them. Others, well, I'd be a little
concerned about spending much time learning to use something that hasn't been updated in 4 years.

So why do we not use these more? Lack of familiarity is one issue: with the VO structure, the idea that 
I have to go to a "registry" to look up a "data service" in order to then look for
the data I want, seems like quite a bit of overhead.  I often know that
I want a specific *kind* of data, and there is only one facility in the world that produces it, so
it's simpler just to go to a specific archive. 
I also haven't used many of the online VO-compliant services like [Iris](http://www.usvao.org/science-tools-services/iris-sed-analysis-tool/) or [VOPlot](http://vo.iucaa.ernet.in/~voi/voplot.htm). Why? It is hard to get used to
the idea of analysing data via a service that runs on some machine far away 
as opposed to somewhere local, where I can see the source code, tweak it if necessary, and
script things to my heart's content. 

The bottom line for me is that, at least for me, the Virtual Observatory is not quite there yet. Some
of the tools look pretty promising and would undoubtedly improve my workflow. Others seems like they are
a lot of talk and not much whiskey, as my grandmother would say.  While astronomers are in an enviable position
as far as the availability of data, our system for gluing it all together (Alyssa Goodman calls this
["Seamless Astronomy"](http://projects.iq.harvard.edu/seamlessastronomy/home)) is still developing. 
I think we are getting there, but aren't quite there yet.



