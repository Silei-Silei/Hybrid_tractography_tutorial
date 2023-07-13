Welcome to the dMRI-microscopy hybrid tractography tutorial
===================================

We propose a data fusion approach to jointly analyse data from dMRI and microscopy that leverages the complementary information these modalities provide about fibre orientations to create hybrid dMRI-microscopy fibre orientations that are both 3D and high specificity and resolution. 

Specifically, we use 2D microscopy to provide detailed estimates of fibre orientation within the microscopy plane and dMRI to provide the out-of-plane orientation. Importantly, we use models that estimate distributions of fibre orientations within dMRI voxels. By extracting the inclination angle for the fibre within this distribution that best matches the in-plane orientation derived from microscopy, we can estimate 3D fibre orientations at spatial resolutions that exceed the dMRI data. 

This hybrid dMRI-microscopy method provides: 
1) 3D fibre orientations; 
2) whole-brain coverage; 
3) high resolution in-plane information. 
The hybrid orientations enable the estimation of complex fibre architecture as described by the microscopy and can then be combined into fibre orientation distributions (FODs) at arbitrary resolutions for input into existing tractography pipelines. 

This tutorial will introduce the code to reconstruct the hybrid orientation, the evaluation of approach and the application to other microscopy contrasts.

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Overview

   Overview

.. toctree::
   :maxdepth: 5
   :hidden:
   :caption: Code Explanation

   Code Explanation

.. toctree::
   :maxdepth: 1
   :hidden:
   :caption: Evaluation

   Evaluation

.. toctree::
   :maxdepth: 1
   :hidden:
   :caption: Different Microscopy Contrast

   Different Microscopy Contrast
