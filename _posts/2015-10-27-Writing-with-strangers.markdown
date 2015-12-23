---
layout: post
title: "Writing with strangers"
date: 2015-10-27
tags: academia publication science
comments: True
---

Strangely enough I am a co-author on a paper to be submitted to [PLoS Computational Biology](http://journals.plos.org/ploscompbiol/).
Aren't you an astronomer, you ask? Why yes. But this journal has a nifty collection of articles
called ["10 Simple Rules"](http://www.ploscollections.org/article/browse/issue/info%3Adoi%2F10.1371%2Fissue.pcol.v03.i01;jsessionid=B9FC1B5AD3661D2CC6F3C15947150DDD) and many are relevant far outside computational biology. 
[Several](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004311) [astronomers](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003542) have published there before.

The [paper](https://peerj.com/preprints/1448/)  is about how scientists should store digital data and I think it
has some interesting ideas. At least as interesting (to me, anyway), is the 
the story of how this paper came to be. The discussion started out as a [GitHub issue](https://github.com/swcarpentry/site/issues/797) on [Software Carpentry](http://software-carpentry.org)'s
site repo, prompted by [Greg Wilson's](http://third-bit.com) [query](http://lists.software-carpentry.org/pipermail/discuss_lists.software-carpentry.org/2015-February/002601.html) to the [Software Carpentry discuss email list](http://lists.software-carpentry.org/mailman/listinfo/discuss_lists.software-carpentry.org). The issue had quite a bit of discussion and 22 participants.

I don't actually remember how [Ted Hart](http://emhart.info/) decided that it would be
a good idea to write a `10 simple rules' paper, but the project 
got its own [repo](https://github.com/emhart/10-simple-rules-data-storage) a little over
a week after the discussion started. Within a few days, [a number of us signed on](https://github.com/emhart/10-simple-rules-data-storage/commits/master/README.md) to work on the project and Ted had proposed
[a timeline](https://github.com/emhart/10-simple-rules-data-storage/issues/24). 
A [bunch of rules](https://github.com/emhart/10-simple-rules-data-storage/issues?utf8=%E2%9C%93&q=label%3A%22Proposed+Rule%22+) were proposed, we discussed them via issues, and Ted attempted to [summarize](https://github.com/emhart/10-simple-rules-data-storage/issues/30).
Each rule got its own issue
and Ted proposed a [writing workflow](https://github.com/emhart/10-simple-rules-data-storage/issues/42) where 
contributors self-assigned themselves to particular rules ([here's mine](https://github.com/emhart/10-simple-rules-data-storage/issues/34)). All of this was done within about 2 months of the discussion starting.

It took a while for everyone to write their stuff, and we did a number of rounds of comments and edits.
(Warning: GitHub jargon ahead.)
The actual writing was done in [markdown](https://help.github.com/articles/github-glossary/#markdown), in [forks](https://help.github.com/articles/github-glossary/#fork) of the [repository](https://help.github.com/articles/github-glossary/#repository), with changes to the
master manuscript submitted as [pull requests](https://help.github.com/articles/github-glossary/#pull-request). (I forget why
we decided to use fork-and-pull rather that direct commits to the repository: easier to guard against mistakes, I think.) [Jeff Hollister](http://jwhollister.com/), [Sarah Mount](http://snim2.org/), and [Naupaka Zimmerman](http://naupaka.net) wrote some [clever
code](https://github.com/emhart/10-simple-rules-data-storage/blob/master/manuscript/makefile) to turn the markdown file into LaTeX and then a PDF automatically.

Things slowed down over the summer, but by 
mid-September things were mostly done and it was time for a [final push](https://github.com/emhart/10-simple-rules-data-storage/issues/74). We got things together, [congratulated ourselves](https://github.com/emhart/10-simple-rules-data-storage/issues/89),
[figured out the author order](https://github.com/emhart/10-simple-rules-data-storage/issues/92),
and put the thing on the [PeerJ Computer Science preprint server](https://peerj.com/preprints/1448/) 
where it awaits comments before being submited to the journal. A few comments are already up
and have been added to the GitHub [issues](https://github.com/emhart/10-simple-rules-data-storage/labels/Pre-Submission%20Revision).

This was a really interesting way to write a paper with a bunch of people that I have never met except
via email and Twitter. At least a few of the authors [have met in person](https://twitter.com/jhollist/status/657524255253471232), though. We were all tolerably proficient at using Git and GitHub, so the pull-request model of making changes worked pretty well.
It's neat to be able to trace the project history through the pull requests and issues, something that would be a lot trickier if one were trying to do it by following an email chain. I am looking forward to the next paper I write this way; it was fun to be involved in such a true collaborative effort.

[v2: Edited to fix link to preprint.]
