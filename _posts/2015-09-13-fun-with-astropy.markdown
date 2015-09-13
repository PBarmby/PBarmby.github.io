---
layout: post
title: "Fun with Astropy"
date: 2015-09-13
tags: astronomy software Python
comments: True
---

In my humble opinion, astronomers could be making more use of the fantastic tools that are in the [astropy](http://www.astropy.org). 
One of the obstacles to this, as identified at the [Python in Astronomy](http://python-in-astronomy.github.io/2015/) workshop, was documentation and worked examples. There are some [tutorials](http://www.astropy.org/astropy-tutorials/) for Astropy already, as well as 
other introductory material for astronomers, but more never hurts.

I was using astropy to do a small task the other day and was really impressed at how the tools in astropy made this very easy.
What I needed to do was take some existing FITS images of M31 and construct masks that could be used to select only pixels that were within specific ranges of M31-o-centric distance. 

I wrote this as a function, because that's how I'm used to doing things. I wouldn't claim it is totally beautiful code, but it's not too terrible. Here it is, hopefully commented well enough to make it understandable.

    import numpy as np
    import astropy.io.fits as fits
    import astropy.units as u
    from astropy.wcs import WCS
    from astropy.coordinates import SkyCoord, Angle, Distance
    from gal_radii_pb import correct_rgc
    
    def do_check(masklist, masklims, save_new_mask=False):
        '''check that masks which are supposed to select only certain galactocentric 
               distances do this correctly
           input: 
           masklist: list of masks to check
           masklims: list of tuples with distance limits corresponding to each mask
           save_new_mask: write out new masks?
           output:
           no return value, but masks may be written to file
           '''
        if len(masklist) != len(masklims):
            print 'first 2 arguments must have same length'
            return
    
        for i, mask in enumerate(masklist):
            # get the limits of galactocentric distance
            lower, upper = masklims[i]
    
            # read in mask to be checked
            maskdat, maskhead = fits.getdata(mask, header=True)
            # set its NaN values to 0
            maskdat[np.isnan(maskdat)]=0
    
            # read mask WCS and construct an array of coordinates
            maskwcs = WCS(maskhead)
            # make an array with the x and y coordinates of each pixel
            pix_indices = np.indices(maskdat.shape) 
            # now compute the corresponding sky coordinates for each pixel
            coords = SkyCoord.from_pixel(pix_indices[1],pix_indices[0],maskwcs,origin=0) 
            # compute galactocentric distance using a specific set of parameters for M31
            galacto_dist = correct_rgc(coords, glx_ctr=SkyCoord(10.724382145*u.deg, 
                                                                41.332205842*u.deg), 
                                               glx_PA=Angle('38d'), 
                                               glx_dist=Distance(780, unit=u.kpc),
                                               glx_incl=Angle('75.883d'))
            # drop the unit on the distance
            galacto_dist_kpc = galacto_dist.to(u.kpc).value 
    
            # construct a new mask with specified distances
            newmask = np.zeros(maskdat.shape) # mask with zeros
            # change only certain pixels to 1
            newmask[np.logical_and(galacto_dist_kpc > lower, 
                                   galacto_dist_kpc < upper)]=1.0 

            # see if the new and old masks are equal
            check = np.array_equal(maskdat, newmask) 
            print '%s %s' % (mask, check)

            # if the masks aren't perfectly equal, see how close they are
            if not check: 
                matches = np.count_nonzero(maskdat==newmask)
                print '%d matches out of %d pix (%f)' % 
                    (matches, maskdat.size, float(matches)/maskdat.size)
            
            # if desired, write out the new mask (with the old header) to a fits file
            if save_new_mask: 
                newname = mask[:-5] + '.check.fits'
                fits.writeto(newname, newmask, maskhead)
        return


This code makes use of a number of the astropy modules including:

* [astropy.io.fits](http://astropy.readthedocs.org/en/latest/io/fits/) to read the data
* [astropy.units](http://astropy.readthedocs.org/en/latest/units/) to deal with units 
* [astropy.wcs](http://astropy.readthedocs.org/en/latest/wcs/) to deal with the [World Coordinate System](http://fits.gsfc.nasa.gov/fits_wcs.html) in the image header, and
* [astropy.coordinates](http://astropy.readthedocs.org/en/latest/coordinates/) to compute angles and distances.

The only non-astropy stuff is `from gal_radii_pb import correct_rgc` --- this refers to a function I wrote myself to compute deprojected galactocentric distances; you can find it [here](https://github.com/PBarmby/pb_utils/blob/master/gal_radii_pb.py). Thanks to [Jonathan Sick](https://gist.github.com/jonathansick) who fixed up the first version of it that I posted.

The nice thing about using astropy is that it hides a lot of the complexity of the computations. Personally, I like this, but I also like that it's an open-source project and I can look at the code if I want to. The important message, though, is that I shouldn't be writing my own code to compute the distance between two coordinates on the sky; someone else has already done it, and probably tested it better than I would. I'd encourage others to explore astropy and its many modules -- a lot of the work you are doing may already be done!



