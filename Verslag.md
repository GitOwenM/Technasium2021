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
Results    6\
Conclusion    7\
Discussion    8

## Introduction
#### Other attempt:
We have two programs (MHCnuggets and Epitope Predictions) which both predict how likely a certain epitope is to be shown on the outside of the cell membrane with different haplotypes. This is important in the recognition of own body cells. If a cell presents an epitope, which is not recognised by the immune system, it will be killed. This presentation of epitopes also plays a key role in vaccine development. In order for a vaccine to be effective you want the epitopes to be presented as often as possible, so the immune system can quickly detect it and develop antibodies against the pathogen. However, these programs output some very different results and thus it is unknown if the given predictions are trustworthy or not. In this paper we discuss the differences between these programs, why they are caused, and how this affects the usefulness of the results. 

------------------------------------------------------------------------------------------------------------------------
#### Previous attempt:
We have two different programs which predict how well peptides bind to MHC complexes, if they bind better the immume system also works better. 

[RJCB: good attempt! Better is more along the lines '[they predict] how well peptides bind to MHC complexes']

This prediction can be used for the development of vaccines. [RJCB: I think the 'but' is funny, I suggest to replace it by a full stop instad :-)]

The two different programs (MHCnuggets and EpitopePredicions) can give very different results. MHCnugets can predict a high value while EpitopePredictions predicts a low value in comparison. In this paper we discuss why these programs output different results.

[RJCB: Again, nice try! Indeed, being able to tell why these programs give different results is nice. But this is not the problem (think a Celcius and Fahrenheit thermometer)]

## Hypothesis
We do not yet have a hypothesis as to why the programs give different results. We suspect it has something to do with the different methods both programs use, but we don’t know enough about this, because we have not figured out how both models work yet.

[RJCB: I enjoy the honesty here! Please keep preferring to do so over bluffing :-)]

## Methods

## Epitope Predictions
Epitope Prediction is one of the programs used for the prediction of IC50 it uses a stabilized matrix to calculate this value. A stabilized matrix is. (Hurwitz matrix?)
It uses the sum of the hydrophobicity value, the physical property of a molecule that is seemingly repelled from a mass of water, of each of the amino acids to calculate how likely they are to appear on the cell membrane. The membrane of a cell is built up of 
This method is faster than the method MHCnuggets uses (neurological network) but this increase in speed may also lead to less accurate results.

Sources:
hydrophobicity
https://en.wikipedia.org/wiki/Hydrophobe

Hurwitz matrix?
https://en.wikipedia.org/wiki/Hurwitz_matrix

Epitope Predictions
https://github.com/jtextor/epitope-prediction

## MHCnuggets

## R-code

## Results
We do not have any results yet.

## Conclusion
None yet.

## Discussion
None, because we have no results yet.

## Definitions
Epitope: the part of an antigen molecule to which an antibody attaches itself. An epitope is a specific protein on the surface of an antigen and is used for recognition of cells.

IC50: a quantitative measure that indicates how much of a particular inhibitory substance (e.g. drug) is needed to inhibit, in vitro, a given biological process or biological component by 50%. The biological component could be an enzyme, cell, cell receptor or microorganism. For our research this means a lower IC50 corresponds to an epitope beine more likely to be presented.

Haplotype: a group of genes within an organism that was inherited together from a single parent. A different haplotype can correspond to a different MHC I-complexe, which in itself means that different epitopes are more or less likely to be presented to the immune system.
