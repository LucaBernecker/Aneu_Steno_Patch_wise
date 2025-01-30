# Patch-Wise Deep Learning Method for Intracranial Stenosis and Aneurysm Detection-the Tromsø Study

This github repository contains the technical implementation of our algorithm for the paper Patch-Wise Deep Learning Method for Intracranial Stenosis and Aneurysm Detection-the Tromsø Study (https://link.springer.com/content/pdf/10.1007/s12021-024-09697-z.pdf).
## Preprocessing
In this repository we present the deep learning core that we invented for classification and detection for intracranial stenosis and aneurysm.

Before applying this algorithm we applied Skull stripping with synthstrip then moved it to MNI-space with ANTSpy (github.com/ANTsX/ANTsPy) and then applied the Fast Fuzzy c-Means Algorithm (https://github.com/YueCui-Labs/FFCM-MRF).


## Core
Afterwards we crop the region of interest, which in our case is the Circle of Willis. Finally we apply the DL core developed by us for detection and classification. 

The core is based on a 50ResNet, that is slided over the image as convolutional window.

Afterwards we make use of a simple deterministic voting algorithm to predict the location. And classify if there is a stenosis or aneurysm. 
