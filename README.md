# AntiSplodge Turorial 

If you are looking for the AntiSplodge python package please visit: https://github.com/HealthML/AntiSplodge/

## Deconvolution of a 10X processed Mouse Brain

![mouse_brain](https://github.com/HealthML/AntiSplodge_Turorial/blob/main/MouseBrain.png "MouseBrain.png")

### Overview

In this tutorial we are gonna demonstrate how to deconvolute the spatial transcriptomics (ST) spots of the adult mouse brain ([10X Adult Mouse Brain](https://support.10xgenomics.com/spatial-gene-expression/datasets/1.1.0/V1_Adult_Mouse_Brain)) utilizing scRNA profiles from the Allen Mouse Brain atlas ([Atlas page](https://portal.brain-map.org/atlases-and-data/rnaseq), [Dataset used](https://portal.brain-map.org/atlases-and-data/rnaseq/mouse-whole-cortex-and-hippocampus-smart-seq)) using the AntiSplodge python package. 

The files needed are found in this repository, and is an exact copy of the datasets, but in numpy structured files for lowered computational requirements and memory usage.

This tutorial is split into four parts:

- Part 1: Prepare single cell (SC) and spatial transcriptomics (ST) datasets
- Part 2: Compute marker genes
- Part 3: Train the AntiSplode model
- Part 4: Deconvolute the ST spots

### Skipping directly to the AntiSplodge part (Part 3 and Part 4)
If you want to get directly to the AntiSplodge part, skip Part 1 and Part 2 and start directly from Part 3. You should still do the imports in Part 1. Doing the scRNA preprocessing will require some amounts of RAM memory. If you intend to do this, all you need is the notebook file (see below) and the files: [SingleCellDatasetOnlyMarkerGenes.h5ad](SingleCellDatasetOnlyMarkerGenes.h5ad) and [SpatialTranscriptomicsDatasetOnlyMarkerGenes.h5ad](SpatialTranscriptomicsDatasetOnlyMarkerGenes.h5ad). 


### Usage

Simply clone the directory to the destination where you intend to run the experiment and open [AntiSplodge_MouseBrain_Tutorial.ipynb](AntiSplodge_MouseBrain_Tutorial.ipynb) in your favorite python notebook IDE.
## Results

In the end you should see an image with spots, like the one shown below. Please note that the scRNA dataset is based on mouse hippocampus and cortex layers, and therefore should used only to get predictions for those regions. If you want to deconvolute the rest of the mouse brain regions, you should look for a matching dataset. 

You should see a image very similar to that of the publication and the one listed below. Notice how the predicted spots are differentiable in the mouse hippocampus, this is exactly what, as the SC dataset is from this particular area. Additinoally, the markers are not as profound as in the paper, this would be better if you increased training time and the number of training/validation samples used.

![mouse_brain](https://github.com/HealthML/AntiSplodge_Turorial/blob/main/showMouseBrainPredictions.png "MouseBrainPredictions.png")

## References

Paper is comming.
