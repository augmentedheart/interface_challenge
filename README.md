<div align='center'>
<h1>AugmentedHeart Interface Challenge</h1>

<h3> 
<a href="https://augmentedheart.com">AugmentedHeart</a>
</h3>

</div>

## Introduction
In this challenge you'll design an inspection tool for viewing a raw ECG signal. We currently work with a Django - React - Postgres setup, which we recommend you use for this challenge as well (Although postgres is probably overkill for this problem, you may use SQLite or similar). If you have a strong preference for another setup, you are free to use that as well, but please don't overcomplicate things. 

## The challenge
For this challenge we ask you to develop an inspection tool containing a plot window for the ECG signal and a list with all annotations. Annotations are defined as binary (arrhyhtmia present or not). In the annotations array there will be intervals in the format (start_index, end_index) as a tuple. All samples within the intervals are assumed 1, all other samples are assumed 0. The goal of the inspection tool is an easy interface for an analist to iterate through all the intervals and either accept or reject the annotation. This should then be saved in a database for later assessment. The analist should be able to move back and forth through the annotations to correct previous decisions. This should in turn also be updated in the database. 

The plot component in particular should be able to:
- Scroll over time
- Show all three leads in a single view in vertical alignment.
- Show the correct background grid line spacing typical for ECGs. The background is a rectangular grid layout with horizontal lines spacing 200ms and vertical lines spacing 0.5mV. (For more info on ECGs check out <a href="https://en.ecgpedia.org/wiki/Main_Page">ECGPedia</a>)
- Implement the option to switch between 200ms and 100ms horizontal axis scaling. Update both the singal and the grid layout.

The design and any additional features you can implement are all up to you.
We'll look at design, loading times, lag, unnecessary complexity and user-friendliness of your program.

## Data format
In this repo you can find the signal.npy (3, samples) and annotations.npy (, samples) files that contain the three lead ECG signal and intervals of interest respectively. The intervals array are starting points that we would like to iterate through in the inspection tool to view for potential arrhythmia. The annotations are based on samples not time. The ECG signal is already converted to mV and is sampled at 125 HZ.


## Submission
When you're satisfied send a zip file of your work to frederik@augmentedheart.com

