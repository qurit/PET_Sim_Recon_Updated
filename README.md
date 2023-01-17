# PET_Sim_Recon_Updated
The Update of PET_Sim_Recon code (i.e., PET simulation and image reconstruction, Link: https://github.com/ashrafinia/PET_sim_recon)


**(1) Important Info. regarding the original code**

Summary:

• Analytic simulation of PET data (with and without noise)

• Begin with your own image, or you can use our included NEMA NU-2 phantom generator

• Enables noisy and noise-free reconstructions.

• Statistical PET image reconstruction framework using 2D ordered-subset expectation maximization (OS-EM) algorithm

• Incorporate attenuation and normalization modeling and correction using a CT sinogram and detector normalization map, respectively.

• Integrated generalized PSF modeling (resolution modeling) to model true PSF, no-PSF, as well as under- and overestimated PSF in reconstruction

• Can vary a range of data acquisition and image reconstruction parameters

• Capable of simulating and reconstructing signal (tumor) absent, i.e. replacing the signal value with the background, as well as signal present, to study the effects of model parameters on the background in the exact same location as the tumor.

Reference:

Please use the following reference if you publish results obtained using this software tool:

S. Ashrafinia, et al., “Generalized PSF modeling for optimized quantitative-task performance”, Phys. Med. Biol., vol. 62, pp. 5149-5179, 2017.

Technical Description:

This Matlab®-based framework incorporates PET forward projection and reconstruction steps.

The framework models many realistic PET reconstruction processes, such as decay of radioactivity, ability to perform attenuation correction using a CT sinogram as well as detector sensitivity normalization using normalization sinogram. The framework is capable of reconstructing noisy and/or noise-free, as well as signal present/absent. For the noisy reconstruction it incorporates realistic random Poisson noise to the data to generate different noise realizations.

A single slice can be loaded as the true image. The PSF modeling has different settings including no PSF, true PSF, and our proposed generalized PSF modeling that uses under-and overestimated PSF kernels in the reconstruction as described in the paper above. The true PSF is derived analytically from modeling PET resolution degradation effects including photon non-collinearity, inter-crystal scattering and inter-crystal penetration, and is being used in the forward projection. In the reconstruction, either the true PSF can be used to model PSF reconstruction. Other PSF kernels are under- or overestimated version of this analytically derived true PSF that was used in the forward projection.

Images are saved at the end of every iteration, for every noise realization, and every PSF setting. The framework provides beginning with (forward projecting) a higher resolution image, while reconstructing a lower resolution image, which is a more realistic representation of imaging objects.

We also include our digital NEMA phantom generation code that generates a NEMA NU-2 image quality phantom according to NEMA standards to use as a true image.

Please being with "Main_Recon.m". More explanation in given in the comments section of each file.

Contact

For support, contributions and questions, please contact s.ashrafinia (at) gmail (dot) com


**(2) Important Info. regarding the updated code**

**Changes from the original code**
1) Compatibility with both Activity and Concentration map (i.e., user can freely choose it)
2) Compatibility with Multi-Unit (i.e., Activity: [Bq], [kBq], [MBq], Concentration: [Bq/ml], [kBq/ml], [MBq/ml])
3) Adding a couple of Up-To-Date Sensitivities for other scanners in addition to that of GE Discovery RX (i.e.,  GE Discovery MI, Siemens Biograph Vision Quadra)
4) Removing the variable "TotalCounts" in the main code to avoid unnecessary confusion; the variable will be used internally in the function "calib_factor"
5) Adding some comments for better clarification and easy usage

  **(2-2) How to Use**
    1) Install the updated code
    2) Open "Main_PET_sim_recon" file
    3) Execute the code as a test
    4) Explore the code and results by changing inputs and parameter values you might want to use

  **(2-3) Improtant Notes**
    1) Current folder in Matlab should be same with the directory of the main file above (i.e., "Main_PET_sim_recon")
    2) The folder "input": directory where you need to save your true image
    3) The folder "output": directory where you will get reconstructed images through this code

**(2-4) Contact**
    Dr. Arman Rahmim (arman.rahmim@ubc.ca) & Mr. Kyung-Nam Lee (leeronaldo001@gmail.com)
