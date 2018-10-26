# Week 4
More work was done on Microscopium app to have the dataset working. I think it's going to be more challenging than we initially thought/take more time.
To get it done, we will need to download the data, process it (still a bit unclear here..), extract freatures, and produce a CSV that will be used to draw our results (with the bokeh app plot drawer). The CSV must contain data for each image in the data set in the following form:
index, info, neighbors, url, x, y

We will do our work on the BBBC021 dataset, which is a set of breast cancer cell images treated with different compounds/drugs and imaged so that their effects on the cells could be investigated.

A portion of the BBBC021 dataset was downloaded, and we started writing a script to illumination correct the images. Because the images come in the 3 different colour channels and 4 quadrants per image, we have to perform illumination correction to account for the variation in the different images being taken. We want to take a median filter of the pixels.

The reason only a small portion of the available dataset was downloaded is because of the sheer size of the complete set. To give an understanding, here is an excerpt from the database: 
"There are 39,600 image files (13,200 fields of view imaged in three channels) in TIFF format. We provide the images in 55 ZIP archives, one for each microtiter plate. The archives are ~750 MB each."
Because there's going to be a lot of tinkering involved, and some of the processes kinda take a long time, we don't want to be waiting overnight to find out there was a bug in the script.

