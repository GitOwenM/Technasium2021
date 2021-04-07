Google Drive:\
https://drive.google.com/drive/folders/1c4bBsIRNIOyva7WZmbAhaMpkHwuGwF0v?usp=sharing

# Title

## Subtitle

## Table of contents

[RJCB: Niet nodig wat mij betreft]

Table of contents    2\
Introduction    3\
Hypothesis    4\
Methods    5\
Biology    6\
Epitope Predictions    7\
MHCnuggets    9\
R-code    10\
Results    11\
Conclusion    12\
Discussion    13\
Definitions    14\
Aantekeningen    15


## Introduction

#### Other attempt:

[RJCB: good stuff here!]

We have two programs (MHCnuggets and Epitope Predictions) which both predict how likely a certain epitope is to be shown on the outside of the cell membrane with different haplotypes. This is important in the recognition of own body cells. If a cell presents an epitope, which is not recognised by the immune system, it will be killed [RJCB: reading it like that makes this appear a bad idea: why is this a good idea?]. This presentation of epitopes also plays a key role in vaccine development [RJCB: connect these two sectences, '... key role, because to be effective ...']. In order for a vaccine to be effective you want the epitopes to be presented as often as possible, so the immune system can quickly detect it and develop antibodies against the pathogen. However, these programs output some very [RJCB: remove 'very', use a quantification instead if there is one] different results and thus it is unknown if the given predictions are trustworthy or not [RJCB: no, both programs may even be right! Compare thermometers that show Celcius and Fahrenheit]. In this paper we discuss the differences between these programs, why they are caused, and how this affects the usefulness of the results. 

## Hypothesis
We do not yet have a hypothesis as to why the programs give different results. We suspect it has something to do with the different methods both programs use, but we don’t know enough about this, because we have not figured out how both models work yet.

[RJCB: I enjoy the honesty here! Please keep preferring to do so over bluffing :-)]

## Methods

## Epitope Predictions

[RJCB: this is not a Method, this is an Introduction, as you are not doing an experiment yet]

Epitope Prediction is one of the programs used for the prediction of an IC50-value. It uses a stabilized matrix to calculate this value [RJCB: reference to the paper here, such as `[1]`. Use scholar.google.com to get a nicely formatted reference]. A stabilized matrix is (https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-6-132) [RJCB: merge with previous line]
It uses the sum of the hydrophobicity value, the physical property of a molecule that is seemingly repelled from a mass of water, of each of the amino acids to calculate how likely they are to appear on the cell membrane [RJCB: great! ]. The membrane of a cell is built up of phospholipids, which are built up of a hydrophobic tail and a hydrophilic head. See the image below [RJCB: Move the knowledge you build upon, i.e. 'the cell membrane is hydrophic' up].
This method is faster than the method MHCnuggets uses (neurological network) but this increase in speed may also lead to less accurate results [RJCB: compare the two programs after both are introduced. Also, where have you found out that EP is actually slower?].
![image](https://user-images.githubusercontent.com/68740180/113837634-5446ac00-978e-11eb-8dc0-3764e02adbed.png)


[RJCB: Sources == awesome! Move these to to the references however. I 
have written down the first one]

Sources:
hydrophobicity
https://en.wikipedia.org/wiki/Hydrophobe

Epitope Predictions
https://github.com/jtextor/epitope-prediction

Stabilized matrix
https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-6-132

Images:
Cell membrane
https://biologydictionary.net/cell-membrane/


## MHCnuggets

[RJCB: I suggest to introduce MHCnuggets to Introduction,
as no experiments are done here]

## R-code

[RJCB: Describe with the Methods are: what is done with EP and MHCnuggets.
Introduce the tools in the introduction]

## Results

We do not have any results yet.
[RJCB: Use the figures in ep_vs_mhcn here]

[RJCB: Describe objectively, without interpretation what the figures show]


## Discussion

None, because we have no results yet.
[RJCB: Interpret the figures in ep_vs_mhcn here]

[RJCB: Interpret the results here. What does it mean? How can that be? What
does it mean to biologists?]


## Definitions

[RJCB: awesome! Keep this in, as some journals require this! Also,
it helps me check your thoughts :-)]

Epitope: the part of an antigen molecule [RJCB: what is 'an antigen molecule'? Also add the definition of it] to which an antibody attaches itself. An epitope is a specific protein on the surface of an antigen and is used for recognition of cells [RJCB: good attempt! Refine: not all presented peptides are epitopes; what makes a peptide
an epitope?].

IC50: a quantitative measure that indicates how much of a particular inhibitory substance (e.g. drug) is needed to inhibit, in vitro, a given biological process or biological component by 50%. The biological component could be an enzyme, cell, cell receptor or microorganism. For our research this means a lower IC50 corresponds to an epitope being more likely to be presented [RJCB: Warm! It it likelier to bind to MHC, making it *then* likelier to be presented. Don't skip the intermediate step here :-) ].

Haplotype: a group of genes within an organism that was inherited together from a single parent. A different haplotype can correspond to a different MHC I-complex, which in itself means that different epitopes are more or less likely to be presented to the immune system [RJCB: Describe how 'different epitopes are more or less likely to be presented to the immune system'. It feels like a shortcut here :-) ].

## References

 * [1] Bianchi, Frans, Johannes Textor, and Geert van den Bogaart. "Transmembrane Helices are an overlooked source of Major Histocompatibility Complex Class I epitopes." Frontiers in immunology 8 (2017): 1118.

