## Metformin-Model
Whole-body PBPK model of metformin (OCT2/MATE DDI victim drug).

### Repository files
Within this repository, we share a whole-body PBPK model of metformin that has been carefully developed using 39 clinical studies of intravenous or oral administration, covering a broad dosing range (0.001–2550 mg). 

This repository contains a PK-Sim snapshot file of the current PBPK model, which contains simulations and the observed data of all clinical studies used for model development and evaluation. 
The present model represents an update of the metformin model presented by Hanke et al. [1]. The current model features the following updates to prevent drug accumulation in tissues and allow a better prediction of terminal elimination t1/2:
- Partition coefficient calculation and cellular permeability calculation methods.
- Updated permeabilities used for mucosa, liver, kidney, and brain (P (intracellular -> interstitial)).
- The solubility in the distal colon and rectum was set to 0 mg/l to minimize absorption in the large intestine without causing accumulation of the drug inside the intracellular space of the mucosa.
   
### Version information
PK-Sim Version 12.

### License
The model is distributed under the [GPLv2 License](https://github.com/Open-Systems-Pharmacology/Suite/blob/develop/LICENSE). 

### Reference
[1] Hanke N, Türk D, Selzer D, Ishiguro N, Ebner T, Wiebe S, Müller F, Stopfer P, Nock V, Lehr T. 
A Comprehensive Whole‑Body Physiologically Based Pharmacokinetic Drug–Drug–Gene Interaction Model of Metformin and Cimetidine in Healthy Adults and Renally Impaired Individuals. Clinical Pharmacokinetics 2020, [https://doi.org/10.1007/s40262-020-00896-w](https://link.springer.com/article/10.1007/s40262-020-00896-w) 
