<div align='center'>
<h1>AugmentedHeart Interface Challenge</h1>

<h3> 
<a href="https://augmentedheart.com">AugmentedHeart</a>
</h3>

</div>

## Introduction
In this challenge you'll design an inspection tool for viewing a raw ECG signal. We currently work with a Django - React - Postgres setup, which we recommend you use for this challenge as well. (SQLite suffices) If you have a strong preference for another setup, you are free to use that as well, but please keep it simple. 

## The challenge
The inspection tool should be able to plot the ECG signal at the various specified annotation intervals with an option for the inspector to accept or reject the annotation.This should then be accordingly updated in the database. The inspector has to be able to move back and forth through the annotations to correct previous made statements. The annotations can be listed on the side in a separate component.

The annotations are defined as binary (arrhythmia present or not). At the specified intervals the annotation is said to be 1. Keep in mind this is mock data, there are no 

The plot component in particular should be able to:
- Scroll over time
- Show all three leads in a single view in vertical alignment.
- Show the correct background grid line spacing typical for ECGS. The background is a rectangular grid layout with horizontal lines spacing 200ms and vertical lines spacing 0.5mV. (For more info on ECGs check out <a href="https://en.ecgpedia.org/wiki/Main_Page">ECGPedia</a>)
- Implement the option to switch between 200ms and 100ms horizontal axis scaling. Update both the singal and the grid layout.

Tip: Don't load the entire signal at once, only surrounding the annotation interval to reduce loading time.

The design and any additional features you can implement are all up to you.
We'll look at design, loading times, lag, unnecessary complexity and user-friendliness of your program.

## Data format
In this repo you can find the signal.npy (3, samples) and annotations.npy (, samples) files that contain the three lead ECG signal and intervals of interest respectively. The intervals array are starting points that we would like to iterate through in the inspection tool to view for potential arrhythmia. The annotations are based on samples not time. The ECG signal is already converted to mV and is 125 HZ.


## Submission
Fork this repository before you start working on it. When you're satisfied send a zip file of the folder to frederik@augmentedheart.com
