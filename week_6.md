# Week 6

## Using ndi rank filters, which means bokeh loads and plots stuff.
The issue with the filters ran deep and requires a few days dedicated work to fix. As such, we have decided to use  a different filter, the ndi rank filters. 
We also found out we were doing things in the wrong order - quadrants needed to be individually illumed, rather than the images stitched first.
With the rank filter issue resolved, we were able to produce a plot using the bokeh app, and provide a working demo on our machines.


## Problem with loading multiple images.
The triumph was short lived. Loading a single image worked fine however when selecting multiple images, they were unable to be drawn coherently on the graph.
While investigating the issue, we printed matrix representation of the images that were to be drawn on the plot, and saw that when selecting a single image, the width of the matrix was 4, but when selecting multiple images the width of the matrix was 3. Not sure what it means but we will ask Juan and Genevieve. It must be something to do with the numpy representation of the loaded image.

## Remote Image
Juan and Genevieve have set up a remote machine on which we are able to install and run microscopium. The remote machine has the benefit of:
  - having a large amount of ram and processing power
  - is able to be connected to and controlled via ssh
  - can run processess on large data sets remotely, sp we dont have to use our own machines to process images (which could take multiple days)
Now that we have access to this we will hopefully be able to use our newly minted script on the full dataset of images!

## Install from command line
We have unfortunately been using microscopium wrong so far when running from the command line. Originally, when we pip installed microscopium, we had not first installed anaconda and established a conda environment. This has been corrected and microscopium is now accessible/referrable to(?) from projects with an anaconda interpreter.



