# Deep Learning Analysis of Defect and Phase Evolution During Electron Beam Induced Transformations in WS<sub>2</sub>

Supplementary code for the paper: https://arxiv.org/abs/1803.05381

In this project, we used a machine learning framework to identify, extract, cluster, analyze, and track defects in a scanning transmission electron microscopy (STEM) movie of 2D material (WS<sub>2</sub>).

This repository contains 3 notebooks. 


1. WS2_Defects_DeepLearning_gmm.ipynb is the main workflow, starting, involving:

    1.1) Generating traning set from the first frame of the image by utilizing Fast Fourier Transform subtraction (FFT-subtraction) to create labels.  
  1.2) Training a fully convolutional neural network (FCNN) for defect identification.  
  1.3) Extraction of defects from all frames using the trained FCNN.  
  1.4) Clustering the extracted defects using a Gausian Mixture Model (GMM).  
  1.5) Tracking the evolution of selected defects and calculating diffusion 
  
  <p align="center">
    <img src="https://github.com/artemmaksov/ORNL-DeepLearningForAtomicScaleDefectTracking/blob/master/MovieClustered_50.gif?raw=true" width="400" height="400" />
  </p>
  
2. WS2_Defects_LocalCryst_PCA.ipynb uses clustered defects to perfrom local crystallographic analysis using principal component analysis (PCA) 

3. WS2_Defects_Markov_Transitions.ipynb uses extracted defect trajectories to calculate transition probabilities.  



