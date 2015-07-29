---
layout: post
title:  "Rows and columns and histograms"
date:   2015-07-29
tags: Python astronomy
comments: True
---

Warning: post below is more technical than usual. I finally figured out something
which had been confusing me for a long time, although I'm sure it's obvious to others. 
My explanation below is partly to solidify my own understanding and partly in case
I'm not the only person confused about this.

I have been working with astronomical images for just about half my life now. 
Usually these come in [FITS](http://fits.gsfc.nasa.gov/fits_documentation.html) format, with the convention that the
pixels are identified in a Cartesian way (*x* increases to the right along
the horizontal axis, and *y* increase to the top along the vertical axis, with pixel
(1,1) in the lower left of the image. Pixel centers are integer coordinates.
My understanding is that neither of these conventions is universal.

Recently I was trying to plot a 2-D histogram using the `histogram2d` function in `numpy`. The idea of a
2-D histogram is that you have a set of points in the *xy* plane, you divide that plane
into bins (which you can also think of as pixels), and count how many points are in
each bin (this number would be the pixels' value).  The [documentation](http://docs.scipy.org/doc/numpy/reference/generated/numpy.histogram2d.html) explains how to
use the function and gives the helpful information that
`the histogram does not follow the Cartesian convention where `x` values are on the abscissa and `y` values on the ordinate
axis. Rather, `x` is histogrammed along the first dimension of the array (vertical), and `y` along the second dimension of the array
 (horizontal).`

What does this helpful information mean? It's a reminder that arrays in Python do not follow
the image conventions that I described above. In Python, array indices are written in
this order: `[row,column]` and when printed, position `[0,0]` is in the upper left.
The array axes are defined such that axis 0 is rows and axis 1 is columns,  meaning that if `data`
is an array and you do something like `data.mean(axis=0)`, you are averaging each column over all 
rows, in other words along the vertical direction. If you do `data.mean(axis=1)`, you are averaging 
each row over all columns, in other words alon the horizontal direction.

This lovely figure from the [Software Carpentry Python lesson](http://swcarpentry.github.io/python-novice-inflammation/) helps explain:

![Completeness plot]({{ site.url }}/stuff/python-operations-across-axes.svg)

`histogram2d` constructs an array by the procedure describe above. 
But the helpful information tells you that you can't just plot the resulting array as an image over the (x,y) data points, 
because the array has the axes interchanged, and it starts at the upper left rather than lower.
To plot the output of histogram2d with the data points, you have to either:
* plot it as an image but accept that you get your `y` values on the horizontal axis
* transpose it using `T` (see [Dave's Matplotlib Basic Examples](http://www.physics.ucdavis.edu/~dwittman/Matplotlib-examples/))
* or rotate it and flip it along one axis (same as transposing; see [2-D Histogram](http://oceanpython.org/2013/02/25/2d-histogram/))

I figured this out because I was trying to make a fancy plot with the 2-D histogram in the middle 
and the associated 1-D histograms along its sides, a bit like 
[this](http://www.astrobetter.com/blog/2014/02/10/visualization-fun-with-python-2d-histogram-with-1d-histograms-on-axes/),
which is based on [this matplotlib example]http://matplotlib.org/examples/pylab_examples/scatter_hist.html
The way to make the 1-D histograms is by summing
the 2-D histogram along one of the axes. Summing on `axis=0` involves averaging each column along rows,
so that should give you the number of objects as a function of your `y` variable, and summing on 
`axis=1` should give you the number as a function of `x`.

Here is a figure which uses this approach, and the [code](https://gist.github.com/PBarmby/5b136d3a30e9b0c2b068) that produced it
(this code actually required two 2-D histograms because of what I'm computing here; [here](https://gist.github.com/PBarmby/c174cae74baafd912a2b)
is a somewhat simpler version).

![Completeness plot]({{ site.url }}/stuff/complete_2d.png)

I hope you find this useful; comments and/or corrections are welcome, either below or via [pull request here](https://github.com/PBarmby/PBarmby.github.io).