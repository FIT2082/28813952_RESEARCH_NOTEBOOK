# Week 11

## UI Improvement: Toggle cluster mode button
Microscopium aims to provide an easy to use and intuitive user inerface that allows for simple data exploration.
In an effort to improve the data exploratioin capabilities, I have begun to add a button group to the app that would allow for users to select what reduction method should be applied to the data.
User can now select to view a plot of tSNE, PCA or UMAP applied to a dataset and explore from there without having to restart the app/reload data.
A very nice benefit of this is that a user can select an image, then change the plot and see where the image lies under different clustering methods. It also means that if one of the methods is better at say, identifying fluff, and another is better at clustering MOAs, we get the benefit of both.

## Poster: Process Diagram, Mock-up
Poster presentation is coming up next week and the drafting process is well underway. Juan and Genevieve have provided a lot of feedback and direction to our mockups (both paper/big picture and on Google Drawings for more detailed comments)
With this the work has been smooth and we have been able to dedicate a bit of time to making a flowchart to explain the microimaging/data exploration process.
So far it's looking good, but there is still plenty to be done. A0 is a big fromat and you can fit a lot of information on it, but I dont want a novel on a page, so a design rule of thumb being used is that the poster should be as readable if scaled own to A4 size.

## Converting Images to JPEGs
There are two major factors slowing down the performance of the microscopium app that both Draga and myself would really like addressed before the presentation (just to make it smoother and quicker).
First is to stop running the app on a remote machine over ssh and instead run it locally. This is becuase we have a lot of images, and intend to load many at once. We don't want to have to send all these images over the internet before loading them. To fix this we simply need to install microscopium locally on our laptops, and copy the data_out directory over.
Second is the image format. The images are currently saved as gigantic TIFF files, which is great for the feature extraction part of the process, but unnecessary here and makes the wait time for loading images really terrible. To fix this we will simply convert the TIFFs to JPGs and load these. This will only require minor edits to the csv that can be done simply and progammatically. 
