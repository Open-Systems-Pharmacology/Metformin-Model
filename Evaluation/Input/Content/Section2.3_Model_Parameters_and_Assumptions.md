### Absorption<a id="model-parameters-and-assumptions-absorption"></a>

The parameter value for `Specific intestinal permeability` and were optimized based on clinical oral data, see [Section 2.3.4](#model-parameters-and-assumptions-identification). The saturable
absorption is implemented via PMAT and OCT1 in the small intestine. As late absorption of orally administered metformin is neither consistent with the reported plasma concentration time-profiles nor with the incomplete absorption of metformin, the relative expression of PMAT and OCT1 in the large intestinal mucosa was set to zero.

No information regarding active transport processes at the basolateral side of the intestinal mucosa could be obtained, therefore, the passive  basolateral permeability) `(P (intracellular -> interstitial)` was optimized, see [Section 2.3.4](#model-parameters-and-assumptions-identification).

The measured solubility in at pH 6.8 was used in the model (see [Section 2.2.1](#invitro-and-physico-chemical-data)).

The dissolution of tablets was implemented via empirical Weibull dissolution. 

### Distribution<a id="model-parameters-and-assumptions-distribution"></a>

Metformin is not bound to plasma proteins (fu = 100 %) (see [Section 2.2.1](#invitro-and-physico-chemical-data)) ([Sirtori 1978](#5-references), [Pentikäinen 1979](#5-references) and [Tucker 1981](#5-references)). A value of 100% was used in this PBPK model for `Fraction unbound (plasma, reference value)`. The major binding partner was set to albumin (see [Section 2.2.1](#invitro-and-physico-chemical-data)).

An important parameter influencing the resulting volume of distribution is lipophilicity. The reported experimental logP ranged from -1.43 was used in this model (see [Section 2.2.1](#in-vitro-and-physicochemical-data)). 

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim®, observed clinical data was best described by choosing the partition coefficient calculation by `PK-SIM Standard` and cellular permeability calculation by `Charged dependent Schmitt normalized to PK-SIM`.

### Metabolism and Elimination<a id="model-parameters-and-assumptions-metabolism"></a>

Following its absorption, metformin is not bound to plasma proteins, not metabolized, and not secreted to bile. Metformin is excreted unchanged with the urine by passive glomerular filtration and active renal secretion through the sequential action of organic cation transporter 2 (OCT2) and multidrug and toxin extrusion protein 1 (MATE1).
The transport protein involved in metformin PK were implemented in the model via Michaelis-Menten kinetics as described below: 

* PMAT

The UGT1A9 expression profiles are based on high-sensitive real-time RT-PCR ([Nishimura 2005](#5-references)). Metabolic enzyme activity was described as saturable process following Michaelis-Menten kinetics, were the `Km`and the `kcat` were optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

* OCT1

The OCT1 expression profiles are based on Microarray expression data ([Kolesnikov 2015](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, were the `Km` was taken from literature and `kcat` was optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

* OCT2

The OCT2 expression profiles are based on Expressed Sequece Tags (EST) ([NCBI 2019](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, were the `Km` was taken from literature and `kcat` was optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

* MATE1

The MATE1 expression profiles assumed 100% expression in the Kidney ([Otsuka 2005](#5-references) and [Masuda 2006](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, were the `Km` was taken from literature and `kcat` was optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

Additionally, passive renal clearance by glomerular filtration was implemented and the `GFR fraction` was set to 1. In addition, fraction of bile that was continuously released was set to 1 (`EHC continuous fraction`)


### Automated Parameter Identification<a id="model-parameters-and-assumptions-identification"></a>

The following parameters have been estimated in the model:

| Model Parameter                |
| ------------------------------ | 
| `Km` (PMAT)             | 
| `kcat` (PMAT)             | 
| `kcat` (OCT1)            |
| `kcat` (OCT2)                    | 
| `kcat` (MATE1)                    | 
| `Specific intestinal permeability`| 
| `Basolateral small intestinal permeability`| 
| `Basolateral large intestinal permeability`| 
| `Tablet dissolution fed Weibull Shape`|
| `Tablet dissolution fed Weibull Time`|


 
