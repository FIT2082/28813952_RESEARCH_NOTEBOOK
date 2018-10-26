# Week 10

This week we processed photos using two different methods.
The feature extraction process identifies the cells in the image and computes various features describing the object.
We have run this process using both a sample of all cells or 100 randomly chosen cells for each image. The idea here is that 100 cells would be likely to be representative of all cells in the image.
It took about 60 hours to process the images with featues from all identified objects, and only about 9 hours for the sample of 100 method.
We expect/hope for very similar results from the clustering on the two datasets, as this would support the idea that the 100 sample method is representative, and would allow for serious performance updates (as demonstrated on the set of 2760 images above). Even if clustering ability drops off a little, it might still be worth it for the amazing performance increase.

## Illumination of Images

After the montaging of the images, we inspected a sample of images and noticed illumination around borders of the four stiched images.
There is a concern that this imperfect illumination may affect the dimension reduction process. A potential way to avoid this is to have the illumination process take a median illumination field over a larger set of images (multiple archives worth), to provide a more representative correction.
This however is not currently a priority, but is something to be investigaed in future. It will be interesting to see if the imperfect illumination does indeed impact the performance of the feature extraction. It might be possible that the imperfect illumination is present in enough images that it becomes a "non feature" and we cluster on cell features anyway.
 
