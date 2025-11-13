### Absorption<a id="model-parameters-and-assumptions-absorption"></a>

The parameter value for `Specific intestinal permeability` was optimized based on clinical oral data, see [Section 2.3.4](#model-parameters-and-assumptions-identification). The saturable
absorption is implemented via PMAT and OCT1 in the small intestine. As late absorption of orally administered metformin is neither consistent with the reported plasma concentration time-profiles nor with the incomplete absorption of metformin, the relative expression of PMAT and OCT1 in the large intestinal mucosa was set to zero. Additionally, no information regarding active transport processes at the basolateral side of the intestinal mucosa could be obtained, therefore, the passive  basolateral permeability `(P (intracellular -> interstitial)` was optimized, see [Section 2.3.4](#model-parameters-and-assumptions-identification).

The measured solubility of metformin hydrochloride
in a phosphate buffer at pH 6.8 was used in the model (see [Section 2.2.1](#invitro-and-physico-chemical-data)).

The dissolution of tablets was implemented via empirical Weibull dissolution. 

### Distribution<a id="model-parameters-and-assumptions-distribution"></a>

Metformin is not bound to plasma proteins (fu = 100 %) (see [Section 2.2.1](#invitro-and-physico-chemical-data)) ([Sirtori 1978](#5-references), [Pentikäinen 1979](#5-references) and [Tucker 1981](#5-references)). A value of 100% was used in this PBPK model for `Fraction unbound (plasma, reference value)`. The major binding partner was set to albumin (see [Section 2.2.1](#invitro-and-physico-chemical-data)).

An important parameter influencing the resulting volume of distribution is lipophilicity. The reported experimental logP of -1.43 was used in this model (see [Section 2.2.1](#invitro-and-physico-chemical-data)). 

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim®, observed clinical data was best described by choosing the partition coefficient calculation by `PK-SIM Standard` and cellular permeability calculation by `PK-SIM Standard`.

The liver, kidney and brain permeabilities (i.e., (`(P (intracellular -> interstitial) liver periportal`, `(P (intracellular -> interstitial) liver pericentral` and (`(P (intracellular -> interstitial) kidney`) were optimized to avoid accumulation of drug in tissue and to capture observed PK profiles [Section 2.3.4](#model-parameters-and-assumptions-identification). 

### Metabolism and Elimination<a id="model-parameters-and-assumptions-metabolism"></a>

Following its absorption, metformin is not bound to plasma proteins, not metabolized, and not secreted to bile. Metformin is excreted unchanged with the urine by passive glomerular filtration and active renal secretion through the sequential action of organic cation transporter 2 (OCT2) and multidrug and toxin extrusion protein 1 (MATE1).
The transport proteins involved in metformin PK were implemented in the model as described below: 

* PMAT

The PMAT expression profiles are based on high-sensitive real-time RT-PCR ([Nishimura 2005](#5-references)). Metabolic enzyme activity was described as saturable process following Hill kinetics, where the `PMAT Hill` was taken from literature and `Km`and `kcat` where optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

* OCT1

The OCT1 expression profiles are based on Microarray expression data ([Kolesnikov 2015](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, where the `Km` was taken from literature and `kcat` was optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

* OCT2

The OCT2 expression profiles are based on Expressed Sequece Tags (EST) ([NCBI 2019](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, where the `Km` was taken from literature and `kcat` was optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

* MATE1

The MATE1 expression profiles assumed 100% expression in the Kidney ([Otsuka 2005](#5-references) and [Masuda 2006](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, where the `Km` was taken from literature and `kcat` was optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

Additionally, passive renal clearance by glomerular filtration was implemented and the `GFR fraction` was set to 1. In addition, fraction of bile that was continuously released was set to 1 (`EHC continuous fraction`)


### Automated Parameter Identification<a id="model-parameters-and-assumptions-identification"></a>

This is the result of the final parameter identification.

| Model Parameter      | Optimized Value | Unit |
| -------------------- | --------------- | ---- |
| `kcat` (PMAT)             | 76.47|1/min|
| `Km` (PMAT)             |367.57 | µmol/l |
| `kcat` (OCT1)            | 641.19 | 1/min |
| `kcat` (OCT2)                    | 17479.74 | 1/min |
| `kcat` (MATE1)                    | 165.69 | 1/min |
| `P(intracellular-interstitial) Kidney`| 4.02E-06 | cm/min |
| `P(intracellular-interstitial) Liver`|4.83E-05 | cm/min |
| `P(intracellular-interstitial) Brain`|0.02 | cm/min |
| `Specific intestinal permeability`| 8.49E-07 | cm/min |
| `P(intracellular-interstitial) mucosa` (Basolateral intestinal permeability)| 2.25E-05 | cm/min |
| `Tablet dissolution fed Weibull Shape`| 0.08 | - |
| `Tablet dissolution fed Weibull Time`| 7.90 | min |


 
