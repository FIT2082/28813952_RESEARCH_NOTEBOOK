# Week 7

## Resolved issue with selecting multiple images
When selecting multiple images in the bokeh app, a different function was called than when a single image is selected.
The function for a single image expects images to be represented as matrices of width 4, each column representing a colour channel in a tiff image. (R,G,B,a where a is the alpha/transparency level of the image). The function called when multiple images are selected expects the images to be represented matricies of width 3 (R,G,B) but was given matricies of width 4.
This results in the images being incorrectly interpreted, even though they are still of course valid numpy matrices.
The fix came by simply calling the same function which was called in single image loading. This function is a wrapper function written for microscopium, and essentially handles the fact that some image processing libraries don't check whether the given images do or do not have an alpha channel.

This may not be a huge fix, but it was enough to earn us our first pull request into microscopium! This was really exciting as I've never done a pull request before and was kinda nervous.

## Remote Machine
We sort of screwed up installing Anaconda on the remote machine, which has a bit of a strange memory division/allocation "thing". We thought it would be easiest to install Anaconda in each of our home directories, but it turned out our home directories share 10GB of space, rather than the 250GB we thought we had. The 250GB live in mnt, but it turns out it's not as trivial as bashing "sudo" a couple of times, to install anaconda distro in mnt and have it available to all the users. Juan is helping us sort out this mess.

Hopefully we will have the data processed soon!

