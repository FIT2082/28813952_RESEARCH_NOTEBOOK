# Week 12

Presentations were this week so obviously the main goal was to analyse the performance of the different clustering algorithms, and finalise the last of the UI improvements ready for the poster.
We managed to find a place which does same day printing, which means we had right up until Thursday to perfect the poster.

## Poster & Presentations
The poster turned our great, and I'm really happy with both the content and how it looks (the flowchart and graphs were great reference tools for the discussion)! A0 is way bigger than I realised.
It was nice to have the same day printing because it mean I got to play with some nitpicky stuff like the (temporary/placeholder) logo and styling, as well as spend a bit more times working on the button group mentioned last week.

## Performance of Microscopium
As discussed last week, we installed microscopium locally and converted the images to be loaded into JPGs.
This provided a considerable, noticeble performace increase, with images loading quickly after being selected, and being able to select mroe images at once, without significant wait times.

We also got to compare the diffrence in clustering performance between the two sampling methods for feature extraction mentioned last week. We did expect similar results, however did find that the plots varied significantly, and shared very very little (to no) resemblance.
In terms of an actual numerical assessment, we ran K nearest neighbours classification algorithm, predicting mode of action from the x and y coordinates of the all cell sample and 100 cell sample data with tSNE, UNAP and PCA applied to each.
The best performing method was found to be tSNE on all cell sample.

## Ahead For the Report
There is a lot to talk about for the report as we've been exposed to a lot of different concepts on this very broad project.
The UI imporvements and performance assessment will feature heavily in the report, but there is a lot to talk discuss in terms of future work.
It will be interesting to compare the performance of the microscopium system as a whole to other classification systems.

Its been a great project, and I offer sincere thanks to Julian, Juan and Genevieve for their tutelage and support.
