# Machine Learning on Neuroscience datasets

## Preparing the data using Panda dataframes:

  The data preparation notebook contains the code written to process the the feature and target vectors.
We used panda dataframes to extract the two gold MSI (The Goldsmiths Musical Sophistication Index) scores for musical training and active musical engagment ( for more info visit : https://www.gold.ac.uk/music-mind-brain/gold-msi/).

  Feature vectors are correlations between the "activation" of different brain voxels according according to BOLD(Blood-oxygen-level dependent) imaging using fMRI data of all the subjects.
  Python module Nilearn allows to manipulate fMRI data and visualization of different Regions of Interest. We used it to get the correlations graphs that served as feature vectors.
  
For copyright issues the original data of the subjects's fMRI and scores are not available.

## Using PLSR to train the model:
Here we use PLSR model ( see more about it on Sklearn) to reduce dimension by keeping the features that explain the best the variance in the scores, a selection of K-best features is done before.
And we used Leave N groups out methode for cross validation.

We also visualize the most relevant brain connections for each feature usign Nilearn functions. ( See pictures below)

![Alt text](active.png?raw=true "lowest pval")
![Alt text](training.png?raw=true "lowest pval")
  
