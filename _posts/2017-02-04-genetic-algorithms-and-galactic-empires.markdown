---
layout: post
title: "Genetic algorithms and galactic empires"
date: 2017-02-04
tags: astronomy physics sf fun
comments: True
---

I had my most-ever-popular tweet last week:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Don&#39;t see a lot of arxiv papers with &quot;humanity&#39;s ultimate goal of a galactic empire&quot; in the abstract but here&#39;s one: <a href="https://t.co/bqhw2xixbm">https://t.co/bqhw2xixbm</a></p>&mdash; Pauline Barmby (@PBarmby) <a href="https://twitter.com/PBarmby/status/827129108190593024">February 2, 2017</a></blockquote>

The "galactic empire" bit obviously caught some attention!
So  what is the paper by Fung, Lewis, and Wu of the University of Sydney,
titled
["The optimisation of low-acceleration interstellar relativistic rocket trajectories using genetic algorithms"](https://arxiv.org/abs/1702.00030)
all about?

Figuring out how to get a rocket where you want it to go involves knowing a number of things:

* where do you want to go? (remember that your target is likely moving, so you want to get to its orbital path *when it's there*)
* how fast do you want to be going when you get there? (often the same speed as your target's orbital speed)
* how much fuel does your rocket have?
* how hard does your rocket engine push? 

"Optimizing a trajectory" in this context refers to working out how to arrive at your destination, with your desired velocity, in the shortest time or using the least fuel. There are lots of options: do you speed up quickly and then coast to your destination, or accelerate more slowly so that you don't have to slow down as much when you get there? This is the kind of problem that may not have an exact mathematical solution: often you have to compute a number of possible solutions and see which one is best ("optimization").

The authors of the paper explain that many researchers have worked on optimizing trajectories for travel between the stars ("interstellar") at low accelerations. Low accelerations are the opposite of what we often think of with rockets leaving Earth, where an enormous force pushes the astronauts down into their seats. High accelerations are needed to escape the Earth's gravity but they use a lot of fuel. Once you're in interstellar (or even interplanetary) space, low accelerations work just fine. They require a lot less fuel, which is important if you want to be able to build a spacecraft that isn't ridiculously large.

Previous papers on interplanetary trajectories have generally assumed that the [curvature of spacetime](http://www.einstein-online.info/spotlights/geometry_force) described by the
[general theory of relativity](http://www.einstein-online.info/spotlights/gr) is so small as to be unimportant. Fung, Lewis, and Wu instead try to solve the rocket equation
(yes, there is such a thing!) by taking general relativity, and a reasonably realistic model of the gravitational field of the Milky Way,
into account. They consider three possible kinds of rockets --- fusion, amtimatter, and photon---which each emit their exhaust products at different speeds and so have different possible accelerations.

The ["genetic algorithm"](http://www.ai-junkie.com/ga/intro/gat1.html) part is a way of getting to the optimal trajectory by simulating how evolution works.
The authors use a computer program that works out an initial set of trajectories and measures how good they are (their "fitness").
The best of this first set are then combined into a new set of trajectories, with some random changes ("mutations"), and the
fitness of this second generation is computed. The best of this generation of trajectories then "reproduces," and so on.
The authors of this paper used 20 generations and discussed the fittest trajectory for each.

Fung, Lewis, and Wu considered 3 possible destinations for their interstellar spaceship: regular stars orbiting within the Milky Way disk,
[hypervelocity stars](https://www.cfa.harvard.edu/oir/sp/hypervel.html) currently located in the disk, and
stars in the [Milky Way halo](https://en.wikipedia.org/wiki/Milky_Way#Halo). For each of these, they consider
stars ahead of the Sun in the direction of [galactic rotation](http://www.universetoday.com/30710/galaxy-rotation/) and stars behind the Sun in the rotation pattern.
These two cases are important because they want the rocket to end up going in the same direction as the stars,
so travelling to stars behind the Sun requires turning around at the end of the trip; see the figures below.

![Trajectory for a rocket travelling to a star behind the Milky Way in Galactic rotation. The Galaxy rotates clockwise in this view.]({{ site.url }}/stuff/flw_fig3.png)
![Close up of above trajectory, at beginning (left) and end (right).]({{ site.url }}/stuff/flw_fig4.png)

Figures 3 and 4 from [Fung, Lewis, and Wu](https://arxiv.org/abs/1702.00030), showing trajectory for a trip to a star behind the Milky Way in Galactic rotation. The Galaxy rotates clockwise in this view. The bottom figure is a close-up of the beginning (left)
and end (right) of the trajectory.

The authors find that the genetic algorithm works, although it's more difficult to get good solutions for trips to stars in the Milky
Way halo. The speeds for the optimum trajectories are less than about 20% of the speed of light, which means that the effects of the
Milky Way's gravity are small. The speeds derived imply that fusion drives are impractical for interstellar journeys since they
would require a spacecraft which is 99-99.999% fuel!
Even for antimatter rockets, which we don't actually know how to build, low-acceleration travel times are hundreds of thousand of years.
Fung, Lewis, and Wu conclude that "galactic colonisation is highly unrealistic using low-acceleration rockets...human expansion into 
the cosmos is extremely unlikely unless high acceleration rockets were used."

The Galactic Republic and the Galactic Empire both seem a long way off.
