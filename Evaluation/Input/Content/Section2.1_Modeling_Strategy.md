The general concept of building a PBPK model has previously been described by Kuepfer et al. ([Kuepfer 2016](#5-references)). Relevant information on anthropometric (height, weight) and physiological parameters (e.g., blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in adults was gathered from the literature and has been previously published ([Willmann 2007](#5-references)). The information was incorporated into PK-Sim® and was used as default values for the simulations in adults.

Transporters and metabolizing enzymes relevant to the pharmacokinetics of the modeled drugs were
implemented in agreement with current literature, utilizing the PK-Sim® expression database ([PK-Sim Ontogeny Database Version 7.3](#5-references)) or otherwise referenced for the specific process.

A model was built based on clinical data from studies with intravenous and oral administration of metformin. The studies reported individual or mean plasma concentrations of metformin. From the 39 studies used for model building and evaluatio, 22 studies reported the corresponding metformin fraction excreted to urine. For the studies reporting intravenous administration, metformin was administered in doses of 0.001 to 1000 mg. For the studies reporting oral administration, metformin was administered in doses of 0.001–2550 mg.

Virtual mean individuals were generated for each study according to the published demographic information, with corresponding age, weight, height, sex, ethnicity, hematocrit and GFR, if available. If no information was provided, a default value was substituted (30 years of age, male, European, mean weight, height, hematocrit and GFR characteristics from the PK-Sim® population database). Virtual mean individuals were generated for each study according to the published demographic information, with corresponding age, weight, height, sex, ethnicity, hematocrit and GFR, if available.

The clinical datasets for metformin PBPK modeling were divided into a model building dataset for model building and a test dataset for model evaluation and verification. Both datasets are presented in [Section 2.2](#22-data-used).

A specific set of parameters ([Section 2.3.4.](#model-parameters-and-assumptions-identification)) were optimized to describe the disposition of metformin using the Parameter Identification module provided in PK-Sim®. To limit the parameters to be optimized during model building, the minimal number of processes necessary to mechanistically describe the pharmacokinetics and drug-drug interactions (DDIs) of the modeled drugs were implemented into the models. The saturable absorption is implemented via PMAT and OCT1 in the small intestine. As late absorption of orally administered metformin is neither consistent with the reported plasma concentration time-profiles nor with the incomplete absorption of metformin, the relative expression of PMAT and OCT1 in the large intestinal mucosa was set to zero. Furthermore, no information regarding active transport processes at the basolateral side of the intestinal mucosa could be obtained. Therefore, the passive permeability from the intracellular to the interstitial space of the small intestinal mucosa was optimized.

Details about input data (physicochemical, *in vitro* and clinical) can be found in [Section 2.2](#22-data-used).

Details about the structural model and its parameters can be found in [Section 2.3](#23-model-parameters-and-assumptions).




