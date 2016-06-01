---
layout: post
title: "Data are difficult"
date: 2016-05-31
tags: astronomy research software data
comments: True
---

I am working with a former grad student of mine to complete the last piece of work for the
[paper](http://arxiv.org/abs/1603.06903) that came out of his MSc thesis. This should be simple ---
part of the paper involved analyzing a large catalog of mid-infrared point sources in M31 that he analyzed, and we're formatting
the catalog so that it can be made available through [IRSA](http://irsa.ipac.caltech.edu/frontpage/). The catalog contains
about 425000 objects and makes a pretty big text file, about 550 MB. So it's a bit of a pain to move around, but 
thanks to services like [CANFAR's VOSpace](http://www.canfar.phys.uvic.ca/vosui/), it's not that bad.

All we thought we would need to do is take the catalog which contained the data that was used for the paper,
explain what all the columns meant, put it in the [IPAC format](http://irsa.ipac.caltech.edu/applications/DDGEN/Doc/ipac_tbl.html) 
and send it off to IRSA. But it's never so easy. 

In addition to the information that we analyzed in the paper, there's a lot of related information that we included
in the catalog in an attempt to be complete. It turned out there were several problems with the bonus information,
because the catalog was made partly by a summer student who worked on the project a couple of years ago, and partly by me, and
these two pieces weren't quite joined together correctly. We didn't catch the problems 
while writing the paper because we weren't using the bonus information for it. Then we noticed that our methods for indicating that
some data were useless were not as good as they needed to be. And so on. 
I ended up spending a fair bit of time writing and testing code to fix the various issues. While many of them could have also been
fixed using the excellent table-manipulation program [TOPCAT](http://www.star.bris.ac.uk/~mbt/topcat/), I wanted the processing to be
scripted so that it would be possible to later figure out what had been done. I should figure out whether to make the 
relevant [GitHub](http://www.github.com) repository public, I suppose.

We didn't have to do all this extra work; the paper would have been publishable without releasing the catalog. Was it worth it?
I think so. Masoud  is moving on to other things and is not planning to work on follow-up. I might do some myself, but I expect there is more
that other people will think of doing. So I hope that by releasing the catalog, we enable more science than might otherwise be the case. 
The costs and benefits of data release in astronomy in general are discussed in the
interesting Twitter thread that starts [here](https://twitter.com/davidwhogg/status/733321650863767552). It's a complex topic that deserves
lots of discussion, but I am pleased to work in a field where releasing data is more common than not. 
