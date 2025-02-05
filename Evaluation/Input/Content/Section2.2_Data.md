### In vitro and physicochemical data <a id="invitro-and-physico-chemical-data"></a>

A literature search was performed to collect available information on physicochemical properties of metformin. The obtained information from literature is summarized in the table below, and was used for model building. Final model parameters are stated in [Section 3.1](#31-metformin-final-input-parameters).

| **Parameter**           | **Unit** | **Value** | Source                               | **Description**                                              |
| :---------------------- | ----------- | --------- | ------------------------------------ | ------------------------------------------------------------ |
| MW                      | g/mol    |  129.16   | [Wishart 2006](#5-references)         | Molecular weight |
| pK<sub>a</sub> (base)   |          |  2.80      | [Desai 2014](#5-references)         | Base dissociation constant |
| pK<sub>b</sub> (base)   |          | 11.50      | [Desai 2014](#5-references)         | Base dissociation constant |
| Solubility (pH 6.8)     | g/L    |  350.90      | [Desai 2014](#5-references)         | Solubility |
| logP                    |          | -1.43     | [Graham 2011](#5-references)| Partition coefficient between octanol and water |
| fu                      | %        | 100      | [Tucker 1981](#5-references), [Pentikäinen 1979](#5-references), [Sirtori 1978](#5-references)            | Fraction unbound                |                       
| PMAT Hill     |    | 3     | [Zhou 2007](#5-references) | PMAT Hill coefficient, Literature value = 2.64         |
| K<sub>m</sub> OCT1     | µmol/L   | 1180.00     | [Chen 2009](#5-references) | OCT1 Michaelis-Menten constant            |
| K<sub>m</sub> OCT2      | µmol/L   | 810.00     | [Chen 2009](#5-references) | OCT2 Michaelis-Menten constant            |
| K<sub>m</sub> MATE1      | µmol/L   | 283.00    | [Yin 2016](#5-references) |  MATE1 Michaelis-Menten constant         |
| Tablet fasted Weibull shape           | -        |  1.36      | [Block 2008](#5-references) | Dissolution profile shape |
| Tablet fasted Weibull time            | min      |  7.90     | [Block 2008](#5-references)                 | Dissolution time (50% dissolved)                             |


### Clinical data <a id="clinical-data"></a>

A literature search was performed to collect available clinical data on metformin in adults. 

The following publications were used for model building (training dataset) and model verification (test dataset):

| **Dose [mg]** | **Dosing** | **PK data** |**Dataset**| **Reference** |
| --------------- | ------------------- | ----------------------- | ----------------- |----------------- |
| 0.00145| iv, bolus, sd |plasma, blood and tissue (kidney,liver, intestines and muscle)|training|[Gormsen 2016](#5-references) |
| 250| iv (15 min), sd |plasma, excretion into urine|training|[Tucker 1981](#5-references)| 
| 500| iv (5 min), sd |plasma, excretion into urine|test|[Pentikäinen 1979](#5-references)| 
| 1000| iv (bolus), sd |plasma, excretion into urine|training|[Sirtori 1978](#5-references)| 
| 0.0008556| po, -, fasted, sd |plasma and tissue (kidney, liver, and muscle)|training|[Gormsen 2016](#5-references)
| 10| po, sol, fasted, sd |plasma, excretion into urine|training|[Stopfer 2018](#5-references)|
| 250| po, tab, fed, qd |plasma, excretion into urine|test|[Somogyi 1987](#5-references)|
| 500| po, -, fasted, sd |plasma, excretion into urine|test|[Wang 2008](#5-references)|
| 500| po, sol, fasted, sd |plasma, excretion into urine, and tissue (kidney)|training|[Boehringer 2018](#5-references)|
| 500| po, tablet, fed, sd |plasma|test|[Caillé 1993](#5-references)|
| 500| po, tablet, fed, sd |plasma, excretion into urine|test|[Gusler 2001](#5-references)|
| 500| po, tablet, fasted, sd |plasma|test|[Najib 2002](#5-references)|
| 500| po, tablet, fasted, sd |plasma, excretion into urine|test|[Pentikäinen 1979](#5-references)|
| 500| po, tablet, fasted, sd |plasma, excretion into urine|test|[Sambol 1996b](#5-references)|
| 500| po, tablet, fasted, sd |plasma, excretion into urine|training|[Stopfer 2016](#5-references)|
| 500| po, tablet, fed, sd |plasma, excretion into urine|test|[Tucker 1981](#5-references)|
| 500| po, tablet, fed, bid |plasma, excretion into urine|test|[DiCicco 2014](#5-references)|
| 500 <sup>(a)</sup>| po, tablet, fasted, bid |plasma|test|[Jang 2016](#5-references)|
| 500 <sup>(a)</sup>| po, tablet, fasted, bid |plasma|test|[Kim 2014](#5-references)|
| 500| po, tablet, fasted, bid |plasma|test|[Manitpisitkul 2014](#5-references)|
| 500 <sup>(a)</sup>| po, tablet, fasted, bid |plasma|test|[Oh 2016](#5-references)|
| 750 <sup>(b)</sup>| po, tablet, fasted, bid |plasma|test|[Cho 2011 ](#5-references)|
| 750 <sup>(b)</sup>| po, tablet, fasted, bid |plasma|test|[Cho 2014](#5-references)|
| 750 <sup>(b)</sup>| po, tablet, fasted, bid |plasma|test|[Ding 2014](#5-references)|
| 850| po, sol, fasted, sd |plasma, excretion into urine|training|[Sambol 1996b](#5-references)|
| 850 <sub>(c)<sub>| po, tablet, fasted, bid |plasma|test|[Chen 2009](#5-references)|
| 850| po, tablet, fasted, sd |plasma|test|[Morrissey 2016](#5-references)|
| 850| po, tablet, fed, sd |blood, plasma|test|[Robert 2003 ](#5-references)|
| 850| po, tablet, fasted, sd |blood, plasma, excretion into urine|test|[Sambol 1995](#5-references)|
| 850| po, tablet, fasted, sd |plasma, excretion into urine|test|[Sambol 1996a](#5-references)|
| 850| po, tablet, fed, sd |plasma, excretion into urine|training|[Sambol 1996b](#5-references)|
| 850| po, tablet, fed, sd |plasma, excretion into urine|training|[Sambol 1996b](#5-references)|
| 850<sup>(c)</sup>| po, tablet, fasted, bid |plasma, excretion into urine|test|[Hibma 2016](#5-references)|
| 850| po, tablet, fasted, tid |plasma|test|[Sambol 1996a](#5-references)|
| 1000| po, tablet, fasted, sd |plasma, excretion into urine|test|[Johansson 2014](#5-references)|
| 1000| po, tablet, fasted, qd |plasma|test|[Gan 2016](#5-references)|
| 1500| po, tablet, fed, qd |plasma|test|[Tucker 1981](#5-references)|
| 1700| po, tablet, fasted, sd |plasma, excretion into urine|training|[Sambol 1996a](#5-references)|
| 2550| po, tablet, fasted, sd |plasma, excretion into urine|training|[Sambol 1996a](#5-references)|

<sup>(a)</sup> first dose 750 mg, second dose (500 mg)

<sup>(b)</sup> first dose 1000 mg, second dose (750 mg)

<sup>(c)</sup> first dose 1000 mg, second dose (850 mg)