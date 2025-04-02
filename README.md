# Mapping-Disease-at-the-Cellular-Level-with-HuBMAP
#### Team members: In-Pyo Baek, Sumanth Devarasetty, Yang Han, Suhas Katari Chaluva Kumar, Nicholas Lucarelli

## What is the Problem?
### The similarities and differences between AKI and CKD are not entirely known in the kidney community. The interplay and overlap between the conditions is not well understood. Qualitative studies also contain inherent biases in training and fatigue.

## Why are we trying to solve it?
### AKI is an acute condition, meaning that it can recover back to normal, or progress to chronicity. Identifying markers that can distinguish the different conditions could be the key to understanding these two conditions. Quantitative measures can also improve research speed and objectivity in image analysis. Additionally, healthy tissue samples are difficult to procure, since healthy patients aren't typically biopsied. 

## How are we trying to solve it?
### We are analyzing two different multi-institutional datasets: 1 from healthy reference patients (no discernable kidney disease), and 1 containing AKI and CKD patients. We are analyzing pathology images with segmented functional tissue units, and quantifying physical features that may be indicative of healthy or diseased tissues. 

## Data Sources
### Healthy reference data:
#### Sourced from the [Human BioMolecular Atlas Program (HuBMAP)](https://portal.hubmapconsortium.org/) 
#### Example of image used can be found [here](https://portal.hubmapconsortium.org/browse/dataset/c9a15ae1d3afcfdb852004d0c714416e)
##### *Entire dataset will be published soon* 
![](Images/HuBMAP.png?raw=true)

### Chronic Kidney Disease and Acute Kidney Injury
#### Sourced from the [Kidney Precision Medicine Project](https://www.kpmp.org/)
#### Example of image used can be found [here](https://atlas.kpmp.org/spatial-viewer/view)
![](Images/KPMP.png?raw=true)

## General Workflow
![](Images/Diagram.png?raw=true)

## Aim 1
### We observe that there tend to be more sclerosed glomeruli in diseased samples. The ratio between functional and sclerosed glomeruli may be a predictor between diseased and non-diseased. Notebook: *notebook location* 
#### Future Aim: Identifying and quantifying interstitial fibrosis between healthy and diseased samples

## Aim 2
### We qualitatively observe that there is more white space between tubules in AKI samples vs CKD. Using the segmented tubules, we further segment the white space within the tubules, and measure the ratio of luminal area to total tubular area. A boxplot of the results are shown below.
![](Images/BoxPlot.png?raw=true)
#### 0 = Healthy, 1 = AKI, 2 = CKD
### We also seek to use deep learning methods to analyze image data. We used the [CLAM github repository](https://github.com/mahmoodlab/CLAM) to run multiple instance learning on image patches from healthy, AKI, and CKD samples, with the slide level labels as ground truth. We achieved accuracy of *insert accuracy here*. Selected high gradient patches for each predicted label below! 
![](Images/CLAM1.jpg?raw=true)
##### *From original CLAM github repository*

## Pain Points
### AWS configuration, data storage.

