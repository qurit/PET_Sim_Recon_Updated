# PET_Sim_Recon_Updated
The Update of PET_Sim_Recon code (i.e., PET simulation and image reconstruction, Link: https://github.com/ashrafinia/PET_sim_recon)


**(1) Main changes from the original code**
1) Compatibility with both Activity and Concentration map (i.e., user can freely choose it)
2) Compatibility with Multi-Unit (i.e., Activity: [Bq], [kBq], [MBq], Concentration: [Bq/ml], [kBq/ml], [MBq/ml])
3) Adding a couple of Up-To-Date Sensitivities for other scanners in addition to that of GE Discovery RX (i.e.,  GE Discovery MI, Siemens Biograph Vision Quadra)
4) Removing the variable "TotalCounts" in the main code to avoid unnecessary confusion.; the variable will be used internally in the function "calib_factor"
5) Adding some comments for better clarification and easy usage of this program

**(2) How to use**
1) Install the original code (Link: https://github.com/ashrafinia/PET_sim_recon)
2) Copy and Paste our updated code into the same directory of original code, and Overwrite it
3) Open "Main_PET_sim_recon" file
4) Execute the code as a test
5) Explore the code and results by changing inputs and parameter values you might want to use

**(3) Improtant Notes**
1) Current folder in Matlab should be same with the directory of the main file above
2) The folder "input": directory where you need to save your true image
3) The folder "output": directory where you will get reconstructed images through this code

**(4) References**
1) Original code: *Ashrafinia S, Mohy-Ud-Din H, Karakatsanis NA, Jha AK, Casey ME, Kadrmas DJ, Rahmim A. Generalized PSF modeling for optimized quantitation in PET imaging. Phys Med Biol. 2017 Jun 21;62(12):5149-5179. doi: 10.1088/1361-6560/aa6911. Epub 2017 Mar 24. PMID: 28338471.*
2) Sensitivity of GE Discovery MI: *Chicheportiche A, Marciano R, Orevi M. Comparison of NEMA characterizations for Discovery MI and Discovery MI-DR TOF PET/CT systems at different sites and with other commercial PET/CT systems. EJNMMI Phys. 2020 Jan 14;7(1):4. doi: 10.1186/s40658-020-0271-x. PMID: 31938953; PMCID: PMC6960280.*
3) Sensitivity of Siemens Biograph Vision Quadra: *Prenosil GA, Sari H, Fürstner M, Afshar-Oromieh A, Shi K, Rominger A, Hentschel M. Performance Characteristics of the Biograph Vision Quadra PET/CT System with a Long Axial Field of View Using the NEMA NU 2-2018 Standard. J Nucl Med. 2022 Mar;63(3):476-484. doi: 10.2967/jnumed.121.261972. Epub 2021 Jul 22. PMID: 34301780.*

**(5) Contact**
1) Regarding original code: Dr. Saeed Ashrafinia (s.ashrafinia@gmail.com)
2) Updataed code: Dr. Arman Rahmim (arman.rahmim@ubc.ca) & Mr. Kyung-Nam Lee (leeronaldo001@gmail.com)
