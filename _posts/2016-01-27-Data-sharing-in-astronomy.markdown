---
layout: post
title: "Data sharing in astronomy"
date: 2016-01-27
tags: astronomy science data
comments: True
---

Lots of excitement recently regarding an [editorial](http://www.nejm.org/doi/full/10.1056/NEJMe1516564) in the 
New England Journal of Medicine about data sharing. Concern was expressed that "people who had nothing to do with 
the design and execution of the study" would "use another group's data for their own ends, possibly stealing from the 
research productivity planned by the data gatherers, or even...to try to disprove what the original investigators had posited."
The authors of the editorial stated that some researchers would characterize the people described above as"research parasites".
Needless to say, this got some people mad. Of course there was
a hashtag [#researchparasites](https://twitter.com/search?q=%23researchparasites), and there were some interesting blog posts, by
[Christie Bahlai](https://practicaldatamanagement.wordpress.com/2016/01/22/a-fundamental-difference-of-opinion/),
[Derek Lowe](http://blogs.sciencemag.org/pipeline/archives/2016/01/22/attack-of-the-research-parasites),
and [Leonid Schneider](https://forbetterscience.wordpress.com/2016/01/22/research-parasitism-and-authorship-rights/).
A [follow-up editorial](http://www.nejm.org/doi/full/10.1056/NEJMe1601087) supported data-sharing in
clinical trials and pushed back against the name-calling.

The whole business is bemusing from the point of view of an astronomer, since our field has a different
relationship with research data compared to biomedical research. Ours is an observational science,
and there's only one sky, which everybody with the right equipment and location can see. Some astronomical
objects change with time, meaning that every observation is potentially unique and irreplacable.
Resources are limited, so it's not always feasible to repeat an observation, and of course, it's also pretty difficult to make
money from astronomical observations.
Research data in astronomy has a long history, starting with ancient records of unaided-eye observations,
through those ancient Greeks and the maddening [magnitude system](http://www.skyandtelescope.com/astronomy-resources/the-stellar-magnitude-system/),
to photographic plates and DAT tapes, continuing to today's multi-terabtye digital databases. 

I don't know the history well enough to give a
full overview; rather, I want to talk about how astronomers think about sharing observational data in the present day.
This is based on my own experience as someone who mostly studies nearby galaxies. In general, people in this field
are not super-secretive about our data: we are mostly studying objects that are already known, rather than
discovering new ones as might be the case with very distant galaxies or extrasolar planets.

In a lot of cases, astronomers in general don't get much choice about sharing data. Most publicly-funded observatories, including
space telescopes run by NASA or ESA, ground-based telescopes run as national facilities ([CFHT](http://www.cfht.hawaii.edu),
[ESO](http://www.eso.org), [CTIO](http://www.ctio.noao.edu), and many others) now maintain archives of all their
observations. Often the authors of the
proposal to obtain the observations have exclusive access to the data for one to two years, the idea being
that since they went to the effort of preparing the proposal, they should get a head start on the analysis.
At private observatories, data tend to be a little more, well, private. I don't think this is all big-telescope
selfishness; in fact it's likely more a question of resources. Running a telescope archive takes computers
and programmers and scientists, and many observatories run on shoestring budgets. Interestingly, the private
Keck Observatory does have an [archive](http://www2.keck.hawaii.edu/koa/public/koa.php), funded by NASA.
Archives can account for a substantial fraction of the research done with a telescope, from
[12% for Keck](http://www.keckobservatory.org/recent/entry/nasa_honors_keck_observatory_for_opening_its_archive_to_the_public),
to [close to half for Hubble](https://archive.stsci.edu/hst/bibliography/pubstat.html).

Telescope archives usually contain raw data and some version of processed data. It's not uncommon
to reprocess data from an instrument multiple times, as understanding of its behaviour improves; 
I think some of the [Spitzer](http://spitzer.caltech.edu) archive was reprocessed half a dozen times.
The level of data that you get from a telescope archive is sometimes sufficient to perform science
with immediately, and sometimes not -- it depends to some extent on how well-funded the archive and
any associated data pipelines are.

It's also common for public observatories to run "treasury" or "legacy" programs, often using large
amounts of telescope time: the groups that propose these programs usually have to promise to make available the
processed data that they generate. The key idea here is that since taxpayers of various nations paid
for the facilities that obtained the data, everyone should have access to them. (In principle, observatories 
could just make the data available in their own countries, but that rarely happens). Some examples
include [NOAO Surveys](http://ast.noao.edu/observing/surveys/), [Gemini Large and Long Programs](http://www.gemini.edu/node/12096)
and [Chandra](http://chandra.harvard.edu) "X-ray Visionary Projects" (!). The data released as 
part of these projects usually is science-ready; the teams that proposed the project usually use the
data to do some of their science, and in the process get it ready to release. The [Sloan Digital Sky Survey](http://www.sdss.org),
which I believe is the most productive ground-based telescope ever, is another example of a Big Project
with Lots of Public Data.

If you are an astronomer not part of a big project, you can just post data on your own website, and
some people do that. Of course, people move and web servers die, so this may not be the best way to
preserve data for posterity. There are places where astronomers can deposit processed data for use by others: 
the [NASA/IPAC Extragalactic Database (NED)](http://ned.ipac.caltech.edu), 
I-don't-know-what-it-stands-for [SIMBAD](http://simbad.u-strasbg.fr/simbad/), some telescope archives 
(e.g., the [DUSTiNGS project](http://irsa.ipac.caltech.edu/data/SPITZER/DUSTiNGS/) at 
[IRSA](http://irsa.ipac.caltech.edu/frontpage/)), and generic data-sharing sites like
[figshare](http://figshare.com) or even [GitHub](http://github.com).
There's a good comprehensive list [here](http://nmsu.libguides.com/c.php?g=206377&p=1361931) -- thanks
NMSU library!

Once this data is out there, how do astronomers find it? Stay tuned for Part 2: The Virtual Observatory..