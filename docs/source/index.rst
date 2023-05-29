dMRI microscopy hybrid orientation reconstruction tutorial
===================================


Diffusion MRI orientation
--------
First, the diffusion MRI orientation is provided by the Ball and stick model using FSL. The signal decay of the diffusion is modelled by an isotropic compartment (Ball) and multiple restricted compartments for fibre orientation (stick). 

| merged_th<i>samples: samples from the distribution on theta
| merged_ph<i>samples: samples from the distribution on phi
| merged_f<i> samples: samples from the distribution on anisotropic volume fraction

: The threshold of anisotropic volume fraction for three fibre population is set at 0.05 and fibre having lower volume fraction than this threshold will be removed. Details of ball and stick model output can be found https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FDT/UserGuide.

: Other diffusion model can also be used such as the constrained spherical deconvolution in mrtrix generating the white matter fibre orientation distribution function (fODF). The peaks will be first extracted from the fODF and the discrete fibre orientation can be input into the hybrid model. 


