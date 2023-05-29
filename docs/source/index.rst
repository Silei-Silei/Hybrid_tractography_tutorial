dMRI microscopy hybrid orientation reconstruction tutorial
===================================


Diffusion MRI orientation
--------
First, the diffusion MRI orientation is provided by the Ball and stick model using FSL. The signal decay of the diffusion is modelled by an isotropic compartment (Ball) and multiple restricted compartments for fibre orientation (stick). 

| merged_th<i>samples: samples from the distribution on theta
| merged_ph<i>samples: samples from the distribution on phi
| merged_f<i> samples: samples from the distribution on anisotropic volume fraction


The threshold of anisotropic volume fraction for three fibre population is set at 0.05 and fibre having lower volume fraction than this threshold will be removed. Details of ball and stick model output can be found https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FDT/UserGuide.


Other diffusion model can also be used such as the constrained spherical deconvolution in mrtrix generating the white matter fibre orientation distribution function (fODF). The peaks will be first extracted from the fODF and the discrete fibre orientation can be input into the hybrid model. 


Microscopy orientation
--------
First, the microscopy orientation has been registered to the dMRI space with FSL tool tirl (https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/TIRL/UserGuide). The voxel coordinate for each microscopic pixel is described by x, y, z coordinates in the diffusion mri space. The fiber orientation is represented by the 3D vector.

.. image:: ./fig1.png
  :width: 200px

Second, to facilitate a comparison between the 3D dMRI fibre orientation and 2D microscopy orientation. The dMRI orientation is projected onto the 2D microscopy plane and onto the normal vector of the plane. Next, the angle difference is calculated.

Third, the dyad sample with the smallest angle to the microscopy orientation on the microscopic plane was selected. The through plane angle of the dyad sample is used for the hybrid orientation reconstruction.

Forth, to reconstruct the 3D hybrid orientation, the microscopy provides the in-plane orientation and the dMRI approximates the orientation going out of the microscopic plane.
