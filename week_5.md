# Week 5

This week saw a lot more work being done to have the microscopium program running on new data, the BBBC021 dataset. While we're still not quite there yet, we've uncovered a bit more about what exactly needs to be done.

First, a portion of the dataset was downloaded, then a python script was created wherein the data processing steps were performed.
The dataset contains 4 images per well image that must be stitched together. Furthermore there are three channels for each image, RGB, that must be stacked to compose a complete, full colour image.
Ideally, the preprocessing steps (those performed before feature extraction), will occur in the following order:
  1. stitching 4 smaller images into one full image
  2. an illumination processess, that will darken all pixels below a certain threshold, and brighten the others.
  3. the stacking of the three RGB layers.

After all this, our images should be ready to have features extracted with the UMAP/t-SNE/PCA algorithm (whichever is chosen) or all three.

The microscopium "suite" provides functions to do most of the above, so what is needed is a wrapper script which performs the directory operations, file name regexing and overall pipeline.

Unfrtunately, we ran into trouble with the find_background_illumination() function for part two, as our current method uses numpy to generate a matrix to store the computed values. However, we are computing over a radius of 521px and this ultimately results in a Python MemoryError. 
We thought for a long time that we were doing something wrong ourselves, perhaps calling it with the wrong arguments, or not loading the images correctly. However upon meeting with Juan we discovered it was actually a known issue with numpy.
Juan has a workaround that does not involve using numpy for this part and will have us using sklearn's percentile filter instead. This is much slower than numpy's filtering __would__ have been, had it worked. Pros and cons I guess...

