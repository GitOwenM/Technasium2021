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

[RJCB: good stuff here!]

We have two programs (MHCnuggets and Epitope Predictions) which both predict how likely a certain epitope is to be shown on the outside of the cell membrane with different haplotypes. This is important in the recognition of own body cells. If a cell presents an epitope, which is not recognised by the immune system, it will be killed [RJCB: reading it like that makes this appear a bad idea: why is this a good idea?]. This presentation of epitopes also plays a key role in vaccine development [RJCB: connect these two sectences, '... key role, because to be effective ...']. In order for a vaccine to be effective you want the epitopes to be presented as often as possible, so the immune system can quickly detect it and develop antibodies against the pathogen. However, these programs output some very [RJCB: remove 'very', use a quantification instead if there is one] different results and thus it is unknown if the given predictions are trustworthy or not [RJCB: no, both programs may even be right! Compare thermometers that show Celcius and Fahrenheit]. In this paper we discuss the differences between these programs, why they are caused, and how this affects the usefulness of the results. 

## Hypothesis
We do not yet have a hypothesis as to why the programs give different results. We suspect it has something to do with the different methods both programs use, but we don’t know enough about this, because we have not figured out how both models work yet.

[RJCB: I enjoy the honesty here! Please keep preferring to do so over bluffing :-)]

## Methods
### How does it work?
In this table we have the temperature in two different units: Celsius and Fahrenheit. If we were to plot this table, we would get the following graph (image x). The x-axis shows the temperature in Celsius and the y-axis shows the temperature in Fahrenheit. In this example it is easy to see the correlation: as we increase the value of the x-axis, the y-axis follows. Such a correlation is not always easy to spot. 

![image](https://user-images.githubusercontent.com/78077905/115678460-ce139380-a351-11eb-9464-ddcd8711bcc3.png)

This example is exactly the same as the previous example, but we added some noise to the measurements. Though, at first glance, it might not seem like there is a clear correlation between the two, a trendline shows that this assumption is false. We still have the same correlation between the temperature in Celsius and the temperature in Fahrenheit. 

![image](https://user-images.githubusercontent.com/78077905/115678566-f00d1600-a351-11eb-9ffc-de2db6c371d9.png)

For our last example we have a graph with random data. Here we see there is no correlation: as we increase the value on the x-axis, the y-axis stays the same, this can be seen using the trendline. 

![image](https://user-images.githubusercontent.com/78077905/115678634-02874f80-a352-11eb-8ef8-a83e2bc23090.png)

We also have a way to quantify this correlation, using the Pearson Correlation Coefficient. 

### Pearson Correlation
Using the Pearson Correlation Coefficient we were able to find a correlation between the results of MHCnuggets and EpitopePredictions for each different haplotype. See the formula down below. 
r = Σ(X<sub>i</sub>-x̄)(Y<sub>i</sub>-ȳ) / √(Σ(X<sub>i</sub>-x̄)<sup>2</sup> Σ(Y<sub>i</sub>-ȳ)<sup>2</sup>)
> [JB:I do not know how to edit formulas in markdown]

r = correlation coefficient \
x<sub>i</sub> = values of the x-variable in a sample \
x = mean of the values of the x-variable \
y<sub>i</sub> = values of the y-variable in a sample \
y = mean of the values of the y-variable \

## Biology
### How are antigens presented to the immune system?
  The HLA (human leukocyte antigen) system is a part of the immune system that determines whether a cell in the body is invasive, like a bacteria, and should thus be killed, or a body’s own cell, like a blood cell or a liver cell. 
  This is usually determined by checking whether the antigen that is presented on a MHC-I (Major Histocompatibility Complex) or a MHC-II molecule. These two molecules have nearly the same name, but differ a fair amount. MHC-I molecules are found on all nucleated cells, cells with a nucleus. However MHC-II molecules are only found on the surfaces of antigen presenting cells (APCs) like macrophages or phagocytes. Thus MHC-I is used for the detection of infected cells by, for example viruses or the detection of bacteria and MHC-II is used for presenting the antigens of a virus or bacteria to other cells in the immune system, for example, T helper cells or B cells.[4]
  For viruses this can be determined when a certain cell is infected and is showing a foreign antigen on one of it’s MHC-I proteins. This antigen can be one of the body’s  known antigens or, when the cell is infected by a virus, the virus’ foreign antigen. If a cell is presenting an antigen a Tc cell will determine whether the antigen is foreign or not, if this is the case the Tc cell will kill the cell by disintegrating it’s membrane with proteins. It will also start cloning itself rapidly to be able to more quickly notify other cells necessary in the defense against the virus.
  For bacteria this process is nearly the same, the only difference is that a bacterium is a cell in itself, a virus is not. Thus a bacterium is able to present an antigen itself in contrast to an infected cell presenting the antigen “for” the virus. Because the virus is unable to present the antigen as it is not a cell.
### How does this relate to ic<sub>50</sub>?
## Epitope Predictions

Epitope Prediction is one of the programs used for the prediction of an IC50-value. It was developed by Johannes Textor, a researcher at the Radboud University in Nijmegen. Epitope Predictions uses a stabilized matrix [1] to calculate this IC-50 value. A stabilized matrix is (info)
It uses the sum of the hydrophobicity value [2], the physical property of a molecule that is seemingly repelled from a mass of water, of each of the amino acids to calculate how likely they are to appear on the cell membrane. This is where MHC class I is important. The MHC I molecule is built up of α- and β-chains [], which differ between haplotypes. These chains form a groove, in which a peptide can bind. The MHC I groove is closed and because of this mostly short epitopes can properly bind to it, though research has shown longer epitopes do sometimes bind to MHC I []. These epitopes are mostly between 9 and 11 amino acids long. However, epitopes with different lengths often use alternative binding grooves, which complicates predictions []. Because of this Epitope Predictions uses epitopes that are 9 amino acids long, because they are most common [3], and to simplify predictions.

![Screenshot_20210408_100850](https://user-images.githubusercontent.com/78077905/113991133-74d83a00-9852-11eb-9d7f-b1acc78b8478.png)

The membrane of a human cell is built up of phospholipids, which consist of a hydrophobic tail and a hydrophilic head. This means that a hydrophobic amino acid is less likely to appear on the outside of a cell membrane. See the image below.

![image](https://user-images.githubusercontent.com/68740180/113837634-5446ac00-978e-11eb-8dc0-3764e02adbed.png)

This method is faster than the method MHCnuggets uses (neurological network) but this increase in speed may also lead to less accurate results (needs testing).

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
Introduce the tools in the introduction] \
The scripts that are used to generate the results can be found here (https://github.com/richelbilderbeek/ep_vs_mhcn). They roughly work as follows: the first script (https://github.com/richelbilderbeek/ep_vs_mhcn/blob/master/create_dataset.R) is used to generate random peptides (line 20 to 31) and after that the two programs MHCnuggets and EpitopePrediction are used to predict the ic50 values of the randomly generated peptides (line 33 to 41), these are stored in the file “ep_vs_mhcn.csv” (line 43). \
[JB: ik weet niet hoe je een hyperlink maakt, dus ik heb ze er eerst maar even zo in gezet]
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
[1] Peters, Bjoern, and Alessandro Sette. "Generating quantitative models describing the sequence specificity of biological processes with the stabilized matrix method." BMC bioinformatics 6.1 (2005): 1-9.

[2] Sanchez-Trincado, Jose L., Marta Gomez-Perosanz, and Pedro A. Reche. "Fundamentals and methods for T-and B-cell epitope prediction." Journal of immunology research 2017 (2017).

[3] Trolle, Thomas, et al. "The length distribution of class I–restricted T cell epitopes is determined by both peptide supply and MHC allele–specific binding preference." The Journal of Immunology 196.4 (2016): 1480-1487.

[4] Janeway, Charles A, and Jr. “The major histocompatibility complex and its functions.” Immunobiology: The Immune System in Health and Disease. 5th edition., U.S. National Library of Medicine (1970).


