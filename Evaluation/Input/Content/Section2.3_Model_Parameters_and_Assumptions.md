### Absorption<a id="model-parameters-and-assumptions-absorption"></a>

The parameter value for `Specific intestinal permeability` was optimized based on clinical oral data, see [Section 2.3.4](#model-parameters-and-assumptions-identification). The saturable
absorption is implemented via PMAT and OCT1, mainly in the small intestine. In the original model, as late absorption of orally administered metformin was considered neither consistent with the reported plasma concentration time-profiles nor with the incomplete absorption of metformin, the relative expression of PMAT and OCT1 in the large intestinal mucosa was set to zero. Additionally, as no information regarding active transport processes at the basolateral side of the intestinal mucosa could be obtained, the passive permeability `P (intracellular -> interstitial)` of the small intestinal mucosa was optimized. In the updated model, to allow capture of late-phase pharmacokinetics following single and multiple oral dosing as well as intravenous administration, the expression profile for OCT1 was switched from Array to RT-PCR. Given the contradictory data regarding colonic absorption of metformin, the default expression in the large intestinal mucosa was kept unchanged. Moreover, in addition to refining the permeability from intracellular to interstitial space of the small intestinal mucosa, respective permeabilities were optimized for cecum, colon ascendens, and colon transversum, while setting the later segments colon descendens, colon sigmoid, and rectum to zero, see [Section 2.3.4](#model-parameters-and-assumptions-identification).

The measured solubility of metformin hydrochloride
in a phosphate buffer at pH 6.8 was used in the model (see [Section 2.2.1](#invitro-and-physico-chemical-data)).

The dissolution of tablets was implemented via empirical Weibull dissolution. 

### Distribution<a id="model-parameters-and-assumptions-distribution"></a>

Metformin is not bound to plasma proteins (fu = 100 %) (see [Section 2.2.1](#invitro-and-physico-chemical-data)) ([Sirtori 1978](#5-references), [Pentikäinen 1979](#5-references) and [Tucker 1981](#5-references)). A value of 100% was used in this PBPK model for `Fraction unbound (plasma, reference value)` (see [Section 2.2.1](#invitro-and-physico-chemical-data)).

An important parameter influencing the resulting volume of distribution is lipophilicity. The reported experimental logP of -1.43 was used in this model (see [Section 2.2.1](#invitro-and-physico-chemical-data)). 

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim®, observed clinical data was best described by choosing the partition coefficient calculation by `PK-SIM Standard` and cellular permeability calculation by `Charge dependent Schmitt normalized to PK-SIM`.

The permeability values between plasma and blood cells (`P (blood cells -> plasma)`, `P (plasma -> blood cells)`) were optimized to address the accumulation in red blood cells and capture the difference between plasma and whole blood metformin data.

### Metabolism and Elimination<a id="model-parameters-and-assumptions-metabolism"></a>

Following its absorption, metformin is not bound to plasma proteins, not metabolized, and not secreted to bile. Metformin is excreted unchanged with the urine by passive glomerular filtration and active renal secretion through the sequential action of organic cation transporter 2 (OCT2) and multidrug and toxin extrusion protein 1 (MATE1).
The transport proteins involved in metformin PK were implemented in the model as described below: 

* PMAT

The PMAT expression profiles are based on high-sensitive real-time RT-PCR ([Nishimura 2005](#5-references)). Metabolic enzyme activity was described as saturable process following Hill kinetics, where the `PMAT Hill` was taken from literature and `Km` and `kcat` where optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

* OCT1

The OCT1 expression profiles are based on high-sensitive real-time RT-PCR ([Nishimura 2005](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, where the `Km` was taken from literature and `kcat` was optimized based on clinical data (see [Section 2.3.4](#model-parameters-and-assumptions-identification)).

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
| `kcat` (OCT2)                    | 51723.79 | 1/min |
| `kcat` (MATE1)                    | 165.69 | 1/min |
| `Specific intestinal permeability`| 4.27E-07 | cm/min |
| `P (intracellular -> interstitial)` (Duodenum)| 2.78E-04 | cm/min |
| `P (intracellular -> interstitial)` (Jejunum)| 2.27E-05 | cm/min |
| `P (intracellular -> interstitial)` (Ileum)| 1.23E-05 | cm/min |
| `P (intracellular -> interstitial)` (Cecum, colon ascendens)| 1.72E-05 | cm/min |
| `P (intracellular -> interstitial)` (Colon transversum)| 6.34E-06 | cm/min |
| `P (blood cells -> plasma)` | 4.16E-08 | cm/min |
| `P (plasma -> blood cells)` | 7.70E-08 | cm/min |
| `Tablet dissolution fed Weibull Shape`| 0.11 | - |
| `Tablet dissolution fed Weibull Time`| 7.90 | min |


 
