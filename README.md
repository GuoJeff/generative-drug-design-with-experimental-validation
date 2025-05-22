# Generative Drug (Candidates) Design with Experimental Validation

Compilation of literature examples of generative drug (**candidates**) design that demonstrates experimental validation *at least* *in vitro*. Examples with also *in vivo* validation are specifically noted.

This compilation builds on our [Review Paper](https://rdcu.be/dLah8) and continues to compile literature examples for an up-to-date resource. 

The review article is the result of an awesome collaboration with [Yuanqi Du](https://yuanqidu.github.io/), [Arian Jamasb](https://jamasb.io/), [Tianfan Fu](https://futianfan.github.io/), [Charlie Harris](https://cch1999.github.io/), [Yingheng Wang](https://isjakewong.github.io/), [Chenru Duan](https://www.crduan.com/), [Pietro Liò](https://www.cl.cam.ac.uk/~pl219/), [Philippe Schwaller](https://people.epfl.ch/philippe.schwaller?lang=en), and [Tom L. Blundell](https://www.bioc.cam.ac.uk/research/blundell)!

## BibTeX Citation
```
@article{du2024machine,
  title={Machine learning-aided generative molecular design},
  author={Du, Yuanqi and Jamasb, Arian R and Guo, Jeff and Fu, Tianfan and Harris, Charles and Wang, Yingheng and Duan, Chenru and Li{\`o}, Pietro and Schwaller, Philippe and Blundell, Tom L},
  journal={Nature Machine Intelligence},
  pages={1--16},
  year={2024},
  publisher={Nature Publishing Group UK London}
}
```

<br>

***Please let me know if any examples are missing!*** 🙂

## Number of papers by year (# / total)

**Before 2024**: 25/68

**2024**: 35/68

**2025**: 8/68

<br>

**Every entry contains the following information:**
1. Publication Date - Paper Link
2. Target - Design Task
3. Model (Input: [Molecular Representation], Output: [Molecular Representation])
4. Hit Rate (Number of synthesized examples with IC50 < 10µM or EC50 < 10µM) - **NOTE**: Designs that underwent manual domain-expert modifications are excluded
5. Outcome (denoted nM if < 100 nM) - Most Potent Design (**NOTE**: Most potent *without* any domain-expert modifications. This is in contrast to our [Review Paper](https://rdcu.be/dLah8) which reports the **final** outcome). Finally, *in vivo* validation is noted here and is not restricted to a *generated molecule*.
6. Notes (if applicable)

<br>

**Examples are presented in chronological order based on the final paper publication date.**
 
 Many papers were first pre-printed on either *ChemRxiv*, *BioRxiv*, or *ArXiv* but for ease of organization, the **final** paper publication date is taken. 
 The only exception is if the paper is still in pre-print stage which is the case for many goal-oriented generation examples because they are so recent (as of writing this statement in June 2024).


------------------------------------------------------------------------------------------------------------------------------------------------------------
<br>
<br>
<br>

# **Distribution Learning**

### These examples pre-train on a dataset and/or fine-tune on a set of known actives. Molecules are then sampled from the fine-tuned model.

<br>

# **2018**

### 1. *De Novo* Design of Bioactive Small Molecules by Artificial Intelligence

**Publication Date**: January 10, 2018 - [Paper Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5838524/)

**Target**: RXR - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 4/5 (80%)

**Outcome**: nM agonist - **Most Potent Design**: EC50 RXRγ = 60 ± 20 nM (*N* = 4 assay replicates)

------------------------------------------------------------------------------------------------------------

### 2. Tuning artificial intelligence on the de novo design of natural-product-inspired retinoid X receptor modulators

**Publication Date**: October 22, 2018 - [Paper Link](https://www.nature.com/articles/s42004-018-0068-1)

**Target**: RXR - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 2/4 (50%)

**Outcome**: µM agonist - **Most Potent Design**: EC50 RXRβ = 15.7 ± 0.8 µM (59 ± 5 SEM) (*N* = at least 2 assay replicates)

------------------------------------------------------------------------------------------------------------

# **2020**

### 3. Discovery of Highly Potent, Selective, and Orally Efficacious p300/CBP Histone Acetyltransferases Inhibitors

**Publication Date**: January 7, 2020 - [Paper Link](https://pubs.acs.org/doi/full/10.1021/acs.jmedchem.9b01721)

**Target**: p300/CBP histone acetyltransferases (HAT) - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 1/1 (100%)

**Outcome** Borderline nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 p300 = 10 nM

**Notes**: Only 1 generated molecule was synthesized. Further manual SAR resulted in a more potent design with *in vivo* validation

------------------------------------------------------------------------------------------------------------

# **2021**

### 4. A Novel Scalarized Scaffold Hopping Algorithm with Graph-Based Variational Autoencoder for Discovery of JAK1 Inhibitors

**Publication Date**: August 24, 2021 - [Paper Link](https://pubs.acs.org/doi/10.1021/acsomega.1c03613)

**Target**: JAK1 - **Design Task**: Scaffold hopping

**Model**: GraphGMVAE (Input: Graph, Output: SMILES)

**Hit Rate**: 7/7 (100%)

**Outcome** nM inhibitor - **Most Potent Design**: IC50 =  5.0 nM

**Notes**: The reference compound for scaffold hopping has an IC50 of 45 nM

------------------------------------------------------------------------------------------------------------

### 5. Combining generative artificial intelligence and on-chip synthesis for de novo drug design

**Publication Date**: June 11, 2021 - [Paper Link](https://www.science.org/doi/10.1126/sciadv.abg3338)

**Target**: LXR - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 17/25 (68%)

**Outcome** µM agonist - **Most Potent Design**: EC50 LXRα = 0.21 ± 0.02 µM (*N* = 3 assay replicates)

**Notes**: Used "microfluidics platform for on-chip chemical synthesis"

------------------------------------------------------------------------------------------------------------

### 6. Beam Search for Automated Design and Scoring of Novel ROR Ligands with Machine Intelligence

**Publication Date**: June 24, 2021 - [Paper Link](https://onlinelibrary.wiley.com/doi/full/10.1002/anie.202104405)

**Target**: RORγ - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 3/3 (100%)

**Outcome** µM agonist - **Most Potent Design**: IC50 LXRα = 0.37 ± 0.05 µM (*N* = at least 4 assay replicates)

------------------------------------------------------------------------------------------------------------

# **2022**

### 7. Discovery of Pyrazolo[3,4-d]pyridazinone Derivatives as Selective DDR1 Inhibitors via Deep Learning Based Design, Synthesis, and Biological Evaluation

**Publication Date**: January 13, 2022 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.1c01205)

**Target**: DDR1 - **Design Task**: *De novo* scaffold-based decoration

**Model**: BiRNN encoder–decoder (Input: SMILES, Output: SMILES)

**Hit Rate**: 2/2 (100%)

**Outcome**: nM (borderline µM) inhibitor - **Most Potent Design**: IC50 = 10.2 ± 1.2 nM

**Notes**: The generated set was virtually screened and 2 compounds with the highest docking scores were synthesized. The authors further performed SAR studies.

------------------------------------------------------------------------------------------------------------

### 8. Effective Reaction-Based De Novo Strategy for Kinase Targets: A Case Study on MERTK Inhibitors

**Publication Date**: March 30, 2022 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jcim.2c00068)

**Target**: MERTK - **Design Task**: Reaction based *de novo* design

**Model**: GRU RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 15/17 (100%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 53.4 nM

**Notes**: RNN model generates building blocks compatible with selected reactions.

------------------------------------------------------------------------------------------------------------

### 9. Recurrent neural network (RNN) model accelerates the development of antibacterial metronidazole derivatives

**Publication Date**: August 15, 2022 - [Paper Link](https://pubs.rsc.org/en/content/articlelanding/2022/ra/d2ra01807a)

**Target**: Bacteria - **Design Task**: *De novo* design

**Model**: GRU RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 0/1 (0%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 *S. aureus* = 28.21 µM

**Notes**: 1 generated compound and 11 of its derivatives were synthesized. Within the 11 derivatives, 2 had IC50 < 10 μM. There were additional actives with a concrete potency measured > 10 μM.

------------------------------------------------------------------------------------------------------------

### 10. Target-Focused Library Design by Pocket-Applied Computer Vision and Fragment Deep Generative Linking

**Publication Date**: October 18, 2022 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.2c00931)

**Target**: CDK8 - **Design Task**: Fragment linking

**Model**: GGNN GNN (Input: Graph, Output: Graph)

**Hit Rate**: 9/43 (21%)

**Outcome**: nM inhibitor - **Most Potent Design**: IC50 = 6.4 nM (*N* = 3 assay replicates)

**Notes**: 2 rounds of generation. First round = 37 synthesized, second round = 6 synthesized. Second round takes the optimal inhibitor found from the first round and generates more linkers.

------------------------------------------------------------------------------------------------------------

### 11. PCW-A1001, AI-assisted de novo design approach to design a selective inhibitor for FLT-3(D835Y) in acute myeloid leukemia

**Publication Date**: November 25, 2022 - [Paper Link](https://www.frontiersin.org/articles/10.3389/fmolb.2022.1072028/full)

**Target**: FLT-3 - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 1/1 (100%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 764 nM

------------------------------------------------------------------------------------------------------------

# **2023**

### 12. Leveraging molecular structure and bioactivity with chemical language models for de novo drug design

**Publication Date**: January 7, 2023 - [Paper Link](https://www.nature.com/articles/s41467-022-35692-6)

**Target**: PI3Kγ - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 3/18 (17%)

**Outcome**: µM inhibitor - **Most Potent Design**: Kd = 63 nM (*N* = 2 assay replicates)

**Notes**: 16 molecules (not the top scoring) were purchased from commercial suppliers resulting in a Kd = 640 nM hit. 2 top scoring compounds were manually synthesized and the most potent design had Kd = 63 nM. Derivatives of the top scoring generated compounds were also synthesized resulting in a compound with IC50 = 6.5 nM.

------------------------------------------------------------------------------------------------------------

### 13. Application of deep generative model for design of Pyrrolo[2,3-d] pyrimidine derivatives as new selective TANK binding kinase 1 (TBK1) inhibitors

**Publication Date**: February 5, 2023 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0223523422009369?via%3Dihub)

**Target**: TBK1 - **Design Task**: Fragment linking

**Model**: Transformer (Input: SMILES, Output: SMILES)

**Hit Rate**: 1/1 (100%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 66.7 nM (*N* = 2 assay replicates)

**Notes**: 1 generated molecule was synthesized with IC50 = 66.7 nM. Further SAR studies resulted in more potent designs.

------------------------------------------------------------------------------------------------------------

### 14. Accelerated Discovery of Macrocyclic CDK2 Inhibitor QR-6401 by Generative Models and Structure-Based Drug Design

**Publication Date**: February 8, 2023 - [Paper Link](https://pubs.acs.org/doi/10.1021/acsmedchemlett.2c00515)

**Target**: CDK2 - **Design Task**: Fragment hopping/linking

**Model**: VAE and transformer (Input: SMILES, Output: SMILES)

**Hit Rate**: 17/23 (74%)

**Outcome**: nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 CDK2/E1 = 0.37 nM

**Notes**: The hit rate is not completely accurate as the authors state some modifications were made on the generated structures for synthesis ease (it is unclear the extent of this). 13 compounds were initially synthesized. The crystal structure for one compound was solved and then a second generation campaign to generate linkers to form **macrocycles** was performed. The final optimal compound was validated ***in vivo***.

------------------------------------------------------------------------------------------------------------

### 15. De Novo Design of Nurr1 Agonists via Fragment-Augmented Generative Deep Learning in Low-Data Regime

**Publication Date**: May 31, 2023 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.3c00485)

**Target**: Nurr1 - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 2/6 (33%)

**Outcome**: µM agonist - **Most Potent Design**: EC50 = 0.07 µM

**Notes**: The model was fine-tuned with 1 known Nurr1 agonist which has an EC50 = 0.4 µM.

------------------------------------------------------------------------------------------------------------

# **2024**

### 16. Prospective de novo drug design with deep interactome learning

**Publication Date**: April 22, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-47613-w)

**Target**: PPARγ - **Design Task**: *De novo* ligand- and structure-based design

**Model**: Graph transformer-LSTM RNN (Input: Graph, Output: SMILES) - model is named `DRAGONFLY`

**Hit Rate**: 2/6 (33%)

**Outcome**: µM agonist - **Most Potent Design**: PPARγ EC50 = 1.5 ± 0.2 µM and PPARδ EC50 = 0.24 ± 0.05 µM
 
**Notes**: The model was fine-tuned with 1 known Nurr1 agonist which has an EC50 = 0.4 µM.

------------------------------------------------------------------------------------------------------------

### 17. Automated design of multi-target ligands by generative deep learning

**Publication Date**: September 11, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-52060-8)

**Target**: Pairs of proteins (FXR+sEH, FXR+THRβ, PPARδ+sEH, AT1+sEH, FFAR1+sEH, AT1+FFAR1) - **Design Task**: *De novo* structure-based design for **dual ligands (targeting both proteins in the pairs)**

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: **Note**: In this repo, molecules with potency < 10 µM are considered actives. In this specific case, since the design task is dual activity ligands, if the potency on one target is < 10 µM but > 10 µM on the other, this will still be considered a hit

**Generative Design Part 1 (see notes)**

FXR+sEH (2/3, 67%)

FXR+THRβ (1/3, 33%)

PPARδ+sEH (2/2, 100% **Note**: 1 extra generated compound here but it possessed a tert-butyloxy group which was *replaced* by a tert-butyl. This involved human intervention so it is not considered a *generated* hit)

**Generative Design Part 2**

AT1+sEH (1/1, 100%)

FFAR1+sEH (N/A, *Note** 1 generated compound was synthesized but the cyclopropyl group was replaced by ethyl. This involved human intervention so it is not considered a *generated* hit)

AT1+FFAR1 (1/1, 100%)

**Note**: None of the compounds in **Part 2** exhibited *dual* activity

**Outcome**: Generally µM affinity - **Most Potent Design**: Since the compounds are meant to be dual activity, no numbers are reported here to not bias the reported number towards a particular target. See Table 1 in the paper.
 
**Notes**: In general, the workflow was extracting known actives from BindingDB and performing clustering. **Generative Design Part 1** focused on the 3 pairs of targets which have known actives overlapping in chemical space. **Generative Design Part 2** tackled protein pairs with less overlap of known actives.

------------------------------------------------------------------------------------------------------------

### 18. Combining de novo molecular design with semiempirical protein–ligand binding free energy calculation

**Publication Date**: November 20, 2024 - [Paper Link](https://pubs.rsc.org/en/content/articlelanding/2024/ra/d4ra05422a)

**Target**: AChE - **Design Task**: *De novo* ligand- and structure-based design

**Model**: Used [DRAGONFLY](https://www.nature.com/articles/s41467-024-47613-w) (Graph transformer-LSTM RNN (Input: Graph, Output: SMILES)) which was previously developed by the authors

**Hit Rate**: 1/1 (100%) - 6-step convergent synthesis

**Outcome**: From the paper: "Specifically, compound 2 showed 31.6% (±0.8%) inhibition at 30 μM and 11% (±2%) inhibition at 10 μM" - **Most Potent Design**: 31.6% inhibition at 30 μM
 
**Notes**: Explored chemical space around Huperzine A (known AChE inhibitor). Tried SMILES and SELFIES - generated 4 molecular libraries and filtered with a scoring function notably encompassing a bioactivity prediction model and RAScore (AiZynthFinder retrosynthesis model surrogate). Top molecules were docked with GOLD (proprietary software) and xTB (open-source semiempirical quantum chemistry software).

------------------------------------------------------------------------------------------------------------

### 19. AI-driven de-novo design and development of non-toxic DYRK1A inhibitors for Alzheimer’s disease

**Publication Date**: December 20, 2024 - [Pre-print Link](https://chemrxiv.org/engage/chemrxiv/article-details/67618eed6dde43c9086f5ab8), Published on May 3, 2025 - [Paper](https://pubs.acs.org/doi/10.1021/acs.jmedchem.5c00512)

**Target**: DYRK1A for Alzheimer's disease - **Design Task**: *De novo* structure-based design

**Model**: Used [Hierarchical Graph Encoder-Decoder](https://proceedings.mlr.press/v119/jin20a.html) (Input: Graph, Output: Graph)

**Hit Rate**: 1/1 (100%)

**Outcome**: nM inhibitor - **Most Potent Design**: 41 ± 3 nM (triplicate assays)
 
**Notes**: Trained an ensemble of QSAR models to property prediction. The generative model in total generated 5 batches of 10,000 molecules. After each generation cycle, the molecules were filtered with the QSAR models and similarity to known inhibitors. Molecules passing the filter were used for transfer learning on the model (by adding them to the initial training set and re-training). The best molecules (around 50) were docked (using Schrödinger Glide XP - *proprietary* software) and 1 selected for synthesis. 229 derivatives of the synthesized molecule were also proposed and assessed by the predictive models - in the end, 7 more were synthesized. Since these analogues were based on the selected molecule and not *generated*, they are not included in the hit rate here.

------------------------------------------------------------------------------------------------------------

### 20. Artificial intelligence-enabled discovery of a RIPK3 inhibitor with neuroprotective effects in an acute glaucoma mouse model

**Publication Date**: December 23, 2024 - [Paper Link](https://journals.lww.com/cmj/fulltext/9900/artificial_intelligence_enabled_discovery_of_a.1374.aspx)

**Target**: RIPK3 - **Design Task**: *De novo*

**Model**: Used ChatGPT 3.5 March 2023 (Input: Natural language text, Output: Natural language text)

**Hit Rate**: N/A (see Notes)

**Outcome**: N/A (see Notes)
 
**Notes**: Used ChatGPT to generate molecules (15 were taken after cross-validating with PubChem - see Supplementary Figure 1). 5/15 compounds were selected for further validation. **These 5 compounds are known compounds previously reported in  literature**. 3 open-source models ([GraphDTA](https://academic.oup.com/bioinformatics/article/37/8/1140/5942970), [MGraphDTA](https://pubs.rsc.org/en/content/articlelanding/2022/sc/d1sc05180f), [WGNNDTA](https://link.springer.com/article/10.1186/s12864-022-08648-9)) were used to predict the affinity of the generated molecules. Discovery Studio 2019 (BIOVIA) was used to perform docking and molecular dynamics simulations to validate the predicted affinities and for ADMET prediction. *In vitro* and *in vivo* validation was performed.

------------------------------------------------------------------------------------------------------------

# **2025**

## 21. Deep lead optimization enveloped in protein pocket and its application in designing potent and selective ligands targeting LTK protein

**Publication Date**: February 20, 2025 - [Paper Link](https://www.nature.com/articles/s42256-025-00997-w)

**Target**: LTK - **Design Task**: *De novo*

**Model**: Equivariant GNN (Input: Graph, Output: Graph)

**Hit Rate**: 6/8 (75%) or 8/8 (100%) - 2 molecules had an IC50 of > 1 µM. It is unclear the concrete value.

**Outcome**: nM inhibitor - **Most Potent Design**: IC50 = 6.60 nM on Ba/F3-CLIP1-LTK cells, EIC50 = 1.36 nM (Fig. 5) - demonstrated *in vivo* efficacy in mice
 
**Notes**: The authors cite this [paper](https://www.nature.com/articles/s41586-021-04135-5) which finds that lorlatinib, a known ALK/ROS1 inhibitor according to this [paper](https://www.nature.com/articles/s41571-022-00639-9), can inhibit CLIP1-LTK. 
           Based on this, the authors first fine-tuned their base model on known ALK inhibitors (1,612 actives and 608 inactives from BindingDB). The fine-tuned model generated 227 inhibitors and 13 were selected based on AutoDock Vina docking scores and predicted ADMET properties. The Supporting Information states that 8 were successfully synthesized but it is unclear if all 13 syntheses were attempted. *In vivo* validation was performed.

------------------------------------------------------------------------------------------------------------

## 22. Accelerating discovery of bioactive ligands with pharmacophore-informed generative models

**NOTE**: The paper discusses additional use cases such as pharmacophore-constrained generation and local chemical space exploration 
          but the focus here is only on the case study with experimental validation

**Publication Date**: March 10, 2025 - [Paper Link](https://www.nature.com/articles/s41467-025-56349-0)

**Target**: PLK1 - **Design Task**: *De novo*

**Model**: Based on "GPT" Decoder Transformer (Input: SMILES, Output: SMILES) - model explicitly trained on pharmacophoric information and is named `TransPharmer`

**Hit Rate**: 3/4 (75%)

**Outcome**: nM inhibitor - **Most Potent Design**: IC50 = 5.1 ± 1.7 nM (N=3 replicates) on PLK1 kinase ADP-Glo assay (Fig. 5b)
 
**Notes**: `Onvansertib` is a known PLK1 inhibitor. The pharmacophoric fingerprint was used for conditional generation of 1 million SMILES with 0.7 temperature (more deterministic sampling). Removing invalid molecules and de-duplication resulted in 178,103 unique SMILES. This set of SMILES were filtered based on physico-chemical properties and structural similarity criteria (such as removing SMILES with pharmacophoric similarity and a similar scaffold to `Onvansertib`). Glide standard precision (SP) and extra precision (XP) docking were then used (proprietary docking software) to prioritize compounds. Best molecules were subjected to MM/GBSA and 4 compounds were selected for synthesis. The most potent compounds were also tested for selectivity.

------------------------------------------------------------------------------------------------------------

## 23. Design, synthesis and bio-evaluation of 2,5-disubstituted thiazole derivatives for potential treatment of acute myeloid leukemia through targeting CDK9

**Publication Date**: April 5, 2025 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0045206825003165#bb0175)

**Target**: CDK9 - **Design Task**: *De novo* fragment linking

**Model**: Encoder-decoder transformer (Input: SMILES, Output: SMILES) - Model is [SyntaLinker-Hybrid](https://www.sciencedirect.com/science/article/pii/S266731852200006X)

**Hit Rate**: 1/1 (100%)

**Outcome**: μM inhibitor - **Most Potent Design**: IC50 = 1.139 μM
 
**Notes**: [SyntaLinker](https://pubs.rsc.org/en/content/articlelanding/2020/sc/d0sc03126g) is a model that takes as input 2 terminal fragments and generates a linker connecting them. The model used in this paper, `SyntaLinker-Hybrid`, extends this model by adding transfer learning and "fragment hybridization". 
           Transfer learning on active compounds bias the model's distribution. "Fragment hybridization" takes terminal fragments from known actives and generates *de novo* linkers. Details on the workflow of `SyntaLinker-Hybrid` as used in this paper are limited and the paper only states that **Compound A4** was indentified using this model.

------------------------------------------------------------------------------------------------------------

<br>
<br>
<br>

# **Goal-oriented/directed Learning**

### These examples either pre-train a conditional generator or pre-train and then couple an optimization algorithm for tailored molecular generation. This information is addionally noted.

<br>

# **2018**

### 1. Adversarial Threshold Neural Computer for Molecular de Novo Design

**Publication Date**: March 23, 2018 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.molpharmaceut.7b01137)

**Target**: Kinases - **Design Task**: *De novo* design

**Model**: Differentiable Neural Computer (DNC) (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement Learning

**Hit Rate**: 0 (see Notes)

**Outcome**: µM agonist - **Most Potent Design**: N/A since no generated molecules were *directly* synthesized.
 
**Notes**: An in-house library was screened to identify high-Tanimoto-similarity molecules to the generated set. Therefore, none of the generated molecules were directly experimentally validated.

------------------------------------------------------------------------------------------------------------

### 2. Entangled Conditional Adversarial Autoencoder for de Novo Drug Discovery

**Publication Date**: September 4, 2018 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.molpharmaceut.8b00839)

**Target**: JAK3 - **Design Task**: *De novo* design

**Model**: Adversarial Autoencoder (AAE) (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Conditional generation (conditioned on binding affinity/activity against JAK3)

**Hit Rate**: 1/1

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 6.73 µM

------------------------------------------------------------------------------------------------------------

# **2019**

### 3. Deep learning enables rapid identification of potent DDR1 kinase inhibitors

**Publication Date**: September 2, 2019 - [Paper Link](https://www.nature.com/articles/s41587-019-0224-x)

**Target**: DDR1 - **Design Task**: *De novo* design

**Model**: VAE (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 4/6

**Outcome**: nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 = 10 nM

**Notes**: Generated, synthesized, and performed *in vitro* and *in vivo* validation within 46 days.
 
------------------------------------------------------------------------------------------------------------

 # **2020**

### 4. Design and Synthesis of DDR1 Inhibitors with a Desired Pharmacophore Using Deep Generative Models

**Publication Date**: December 1, 2020 - [Paper Link](https://chemistry-europe.onlinelibrary.wiley.com/doi/10.1002/cmdc.202000786)

**Target**: DDR1 - **Design Task**: *De novo* ligand-based design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES) - Model is `REINVENT`

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 4/6

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 92.5 nM

**Notes**: Pharmacophore matching approach.

------------------------------------------------------------------------------------------------------------

 # **2022**

### 5. Generative and reinforcement learning approaches for the automated de novo design of bioactive compounds

**Publication Date**: October 18, 2022 - [Paper Link](https://www.nature.com/articles/s42004-022-00733-0)

**Target**: EGFR - **Design Task**: *De novo* design

**Model**: Stack-GRU RNN (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 4/15

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 210 nM

------------------------------------------------------------------------------------------------------------

### 6. Generative deep learning enables the discovery of a potent and selective RIPK1 inhibitor

**Publication Date**: November 12, 2022 - [Paper Link](https://www.nature.com/articles/s41467-022-34692-w)

**Target**: RIPK1 - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Conditional generation

**Hit Rate**: 4/8

**Outcome**: µM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 = 35.0 nM

**Notes**: The pre-trained model was fine-tuned via transfer learning and the generate set was virtually screened. This is an example of how generative design and virtual screening can be complementary.

------------------------------------------------------------------------------------------------------------

 # **2023**

### 7. AlphaFold accelerates artificial intelligence powered drug discovery: efficient discovery of a novel CDK20 small molecule inhibitor

**Publication Date**: January 10, 2023 - [Paper Link](https://pubs.rsc.org/en/content/articlelanding/2023/sc/d2sc05709c)

**Target**: CDK20 - **Design Task**: *De novo* structure-based design

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 6/13

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 CDK20/CycT1 = 33.4 ± 22.6 nM

**Notes**: First experimental validated example that used an AlphaFold structure for structure-based design. 2 rounds of generation. There were also additional actives with a concrete measured potency > 10 µM.

------------------------------------------------------------------------------------------------------------

### 8. Discovery of Potent, Selective, and Orally Bioavailable Small-Molecule Inhibitors of CDK8 for the Treatment of Cancer

**Publication Date**: April 7, 2023 - [Paper Link](https://pubs.acs.org/doi/full/10.1021/acs.jmedchem.2c01718)

**Target**: CDK8 - **Design Task**: *De novo* structure-based design

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 1/1

**Outcome**: nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 = 0.4 ± 0.1 nM

**Notes**: The molecule was further optimized by manual domain-expert SAR ultimately resulting in *in vivo* vaidation.

------------------------------------------------------------------------------------------------------------

### 9. De Novo Design of κ-Opioid Receptor Antagonists Using a Generative Deep-Learning Framework

**Publication Date**: August 9, 2023 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jcim.3c00651)

**Target**: KOR - **Design Task**: *De novo* structure-based design

**Model**: VAE (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 2/5

**Outcome**: µM antagonist - **Most Potent Design**: Ki = 6.46 μM

------------------------------------------------------------------------------------------------------------

### 10. Discovery of novel and selective SIK2 inhibitors by the application of AlphaFold structures and generative models

**Publication Date**: August 15, 2023 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0968089623002626)

**Target**: SIK2 - **Design Task**: *De novo* structure-based design (core scaffold was fixed)

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 6/6

**Outcome**: nM inhibitor - **Most Potent Design**: IC50 = 0.023 μM / 23 nM

**Notes**: Used an AlphaFold structure for structure-based design.

------------------------------------------------------------------------------------------------------------

 # **2024**

### 11. Discovery of Novel and Potent Prolyl Hydroxylase Domain-Containing Protein (PHD) Inhibitors for The Treatment of Anemia

**Publication Date**: January 8, 2024 - [Paper Link](https://pubs.acs.org/doi/full/10.1021/acs.jmedchem.3c01932)

**Target**: PHD enzymes - **Design Task**: *De novo* structure-based design

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 1/1

**Outcome**: nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 PHD2 = 4 nM

**Notes**: Further SAR studies were performed by domain-experts, ultimately leading to *in vivo* validation.

------------------------------------------------------------------------------------------------------------

### 12. Local Scaffold Diversity-Contributed Generator for Discovering Potential NLRP3 Inhibitors

**Publication Date**: January 23, 2024 - [Paper Link](https://pubs.acs.org/doi/full/10.1021/acs.jcim.3c01818)

**Target**: NLRP3 - **Design Task**: *De novo* design with an activity model

**Model**: GRU RNN-transformer (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 0 (see Notes)

**Outcome**: N/A - no generated molecules were *directly* synthesized and tested

**Notes**: 12 generated molecules were selected for docking and analysis of the binding poses short-listed two scaffolds. Derivatives were designed based on these two scaffolds, resulting in a nM inhibitor.

------------------------------------------------------------------------------------------------------------

### 13. Discovery of new antiviral agents through artificial intelligence: In vitro and in vivo results

**Publication Date**: January 25, 2024 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0166354224000263?via%3Dihub#bib11)

**Target**: Neuraminidase (NA) of influenza A and B viruses - **Design Task**: *De novo* structure-based design

**Model**: GNN, specifically Attentive FP first described [here](https://pubs.acs.org/doi/10.1021/acs.jmedchem.9b00959) (Input: Graph, Output: Graph)

**Optimization Algorithm Class**: Reinforcement learning (Q-learning)

**Hit Rate**: 2/9 (22%)

**Outcome**: μM inhibitor, antiviral activity with *in vivo* validation - **Most Potent Design**: Quoted from paper: "EC50 0.4 μM against A/St. Petersburg/63/2020, 0.29 μM against A/Vladivostok/2/2009, and 0.74 μM against B/Samara/32/2018 strains (Fig. 4A)"

**Notes**: *in vivo* validation was demonstrated.

------------------------------------------------------------------------------------------------------------

### 14. Quantum Computing-Enhanced Algorithm Unveils Novel Inhibitors for KRAS

**Publication Date**: February 13, 2024 - [Pre-print Link](https://arxiv.org/abs/2402.08210)

**Target**: KRAS - **Design Task**: *De novo* structure-based design 

**Model**: Quantum Computer-LSTM RNN (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Classical optimizer

**Hit Rate**: 1/12 (8%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 1.4 μM

**Notes**: First example of a quantum computer application with experimental validation. There were also additional actives with a concrete measured potency > 10 µM.

------------------------------------------------------------------------------------------------------------

### 15. Generate What You Can Make: Achieving in-house synthesizability with readily available resources in de novo drug design

**Publication Date**: March 5, 2024 - [Pre-print Link](https://chemrxiv.org/engage/chemrxiv/article-details/65e51a8466c138172921935f)

**Target**: MGLL - **Design Task**: *De novo* design with an activity model

**Model**: Graph transformer (Input: Graph, Output: Graph)

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 1/3 (33%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 1 μM

**Notes**: Generation using in-house collection of building blocks.

------------------------------------------------------------------------------------------------------------

### 16. A small-molecule TNIK inhibitor targets fibrosis in preclinical and clinical models

**Publication Date**: March 8, 2024 - [Paper Link 1](https://www.nature.com/articles/s41587-024-02143-0) - [Paper Link 2](https://pubs.acs.org/doi/10.1021/acs.jmedchem.4c01580) - [Blog Post](https://insilico.com/blog/first_phase2) - 

**Target**: TNIK - **Design Task**: *De novo* structure-based design

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: Unknown

**Outcome**: nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 = 4.8 nM

**Notes**: Initial generation led to a nM potent compound but with poor ADMET properties resulting in high clearance in human and mice liver microsomes. Lead optimization led to improved ADMET properties and ultimately *in vivo* validation. 

***Notably, Phase 1 clinical trial results were reported and this molecule is the first generative design to progress to phase 2 clinical trials.***

------------------------------------------------------------------------------------------------------------

### 17. Accelerating factor Xa inhibitor discovery with a de novo drug design pipeline

**Publication Date**: March 11, 2024 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0968089624000762?via%3Dihub)

**Target**: Factor Xa - **Design Task**: Scaffold-based

**Model**: Attention-convolution layers (Input: Substructure vector, Output: SMILES)

**Optimization Algorithm Class**: Mixed-Integer NonLinear Programming from this [Paper](https://aiche.onlinelibrary.wiley.com/doi/full/10.1002/aic.17748)

**Hit Rate**: Unknown (see Notes)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 34.57 μM

**Notes**: 8 commercially available generated molecules were purchased. Only the most potent affinity was reported.

------------------------------------------------------------------------------------------------------------

### 18. PocketFlow is a data-and-knowledge-driven structure-based molecular generative model

**Publication Date**: March 11, 2024 - [Paper Link](https://www.nature.com/articles/s42256-024-00808-8)

**Target**: HAT1 and YTHDC1 - **Design Task**: *De novo* design

**Model**: Flow (Input: Geometry, Output: Geometry)

**Optimization Algorithm Class**: Conditional generation (conditioned on protein pocket)

**Hit Rate**: 0/2 (0%) and 0/3 (0%)

**Outcome**: µM inhibitors - **Most Potent Design**: For HAT1: IC50 = 72.36 ± 8.03 μM and for YTHDC1: IC50 = 32.60 ± 2.72 μM (*N* = 3 assay replicates)

**Notes**: There were also additional actives with a concrete measured potency > 10 µM.

------------------------------------------------------------------------------------------------------------

### 19. Generative AI for designing and validating easily synthesizable and structurally novel antibiotics

**Publication Date**: March 22, 2024 - [Paper Link](https://www.nature.com/articles/s42256-024-00809-7)

**Target**: Bacteria - **Design Task**: *De novo* design with an activity model

**Model**: Monte Carlo Tree Search (MCTS) (Input: Variable, Output: Variable). The activity model takes variable input/output.

**Optimization Algorithm Class**: Monte Carlo Tree Search (MCTS)

**Hit Rate**: 6/58 (10%) - 70 generated molecules were ordered from Enamine and 58 were successfully syntehsized with purity > 90% in ~4 weeks time.

**Outcome**: µM inhibitor with *in vivo* validation. 6 were bioactive against *A. baumannii ATCC 19606R* - **Most Potent Designs**: MIC ≤ 8 µg ml−1

**Notes**: Enforced chemical reactions as permitted transformations during generation.

------------------------------------------------------------------------------------------------------------

### 20. Abstract 5727: ISM9682A, a novel and potent KIF18A inhibitor, shows robust antitumor effects against chromosomally unstable cancers

**Publication Date**: March 22, 2024 - [Paper Link](https://aacrjournals.org/cancerres/article/84/6_Supplement/5727/741278/Abstract-5727-ISM9682A-a-novel-and-potent-KIF18A)

**Target**: KIF18A - **Design Task**: *De novo* structure-based design

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: Unknown (see Notes)

**Outcome**: *in vivo* validation.

**Notes**: 110 molecules were synthesized and tested - [Source](https://www.genengnews.com/topics/artificial-intelligence/insilico-joins-scramble-to-treat-solid-tumors-by-targeting-kif18a/).

------------------------------------------------------------------------------------------------------------

### 21. A dual diffusion model enables 3D molecule generation and lead optimization based on target pockets

**Publication Date**: March 26, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-46569-1)

**Target**: CDK2 - **Design Task**: *Lead optimization*

**Model**: Diffusion (Input: Geometry, Output: Geometry)

**Optimization Algorithm Class**: Conditional generation (conditioned on protein pocket)

**Hit Rate**: 7/7

**Outcome**: nM inhibitor - **Most Potent Design**: IC50 CDK2/E1 = 0.090 nM

**Notes**: Original reference compound has an IC50 CDK2/E1 = 8.1 nM. 2 rounds of generation: 4 molecules synthesized from round 1 resulting in the most potent design IC50 CDK2/E1 = 0.253 nM. 
The second round of focused on intra-linking the molecules resulting in macrocycles. 3 were synthesized and the final most potent design IC50 CDK2/E1 = 0.090 nM.

------------------------------------------------------------------------------------------------------------

### 22. Discovery of 3-hydroxymethyl-azetidine derivatives as potent polymerase theta inhibitors

**Publication Date**: April 1, 2024 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0968089624000762?via%3Dihub)

**Target**: Polθ - **Design Task**: Fragment linking

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 4/6 (33%)

**Outcome**: µM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 = 126.1 μM

**Notes**: Further SAR studies ultimately led to *in vivo* validation.

------------------------------------------------------------------------------------------------------------

### 23. Quantum-assisted fragment-based automated structure generator (QFASG) for small molecule design: an in vitro study

**Publication Date**: April 3, 2024 - [Paper Link](https://www.frontiersin.org/articles/10.3389/fchem.2024.1382512/full)

**Target**: CAMKK2 and ATM - **Design Task**: Fragment linking

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 2/3 (66%) and 1/3 (33%)

**Outcome**: µM inhibitors - **Most Potent Design**: For CAMKK2: IC50 = 3 μM and for ATM: IC50 = 4 μM

------------------------------------------------------------------------------------------------------------

### 24. Identification of SARS-CoV-2 Mpro inhibitors through deep reinforcement learning for de novo drug design and computational chemistry approaches

**Publication Date**: April 29, 2024 - [Paper Link](https://pubs.rsc.org/en/Content/ArticleLanding/2024/MD/D4MD00106K)

**Target**: SARS-CoV-2  - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES) - Model is `REINVENT`

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 1/16 (6%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 3.27 μM (Figure 4)

**Notes**: Combined both distribution learning and goal-directed generation. 17 molecules were ordered from Enamine REAL with 16/17 successfully synthesized and tested.

------------------------------------------------------------------------------------------------------------

### 25. Discovery of a Novel and Potent Cyclin-Dependent Kinase 8/19 (CDK8/19) Inhibitor for the Treatment of Cancer

**Publication Date**: May 1, 2024 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.4c00248)

**Target**: CDK8/19 - **Design Task**: *De novo* structure-based design with some fixed moieities (based on known binder)

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: N/A (see Notes)

**Outcome**: N/A (see Notes)

**Notes**: Compounds were manually designed based on generated molecules and 12 total compounds were synthesized. 
In the end, *in vitro* studies using murine CDX model for human mantle cell lymphoma showed IC50 = 1.34 nm. *In vivo* validation was achieved.

------------------------------------------------------------------------------------------------------------

### 26. Generative Active Learning For The Search of Small-molecule Protein Binders 

**Publication Date**: May 2, 2024 - [Pre-print Link](https://arxiv.org/abs/2405.01616)

**Target**: CDK8/19 - **Design Task**: *De novo* structure-based design with some fixed moieities (based on known binder)

**Model**: MPNN GNN (Input: Graph, Output: Graph)

**Optimization Algorithm Class**: Reinforcement learning (PPO)

**Hit Rate**: N/A (see Notes)

**Outcome**: N/A (see Notes)

**Notes**: 35 analogues of the generated molecules were synthesized. 23/35 have IC50 < 10 μM. The most potent design has IC50 = 0.43 μM.

------------------------------------------------------------------------------------------------------------

### 27. NGT: Generative AI with Synthesizability Guarantees Identifies Potent Inhibitors for a G-protein Associated Melanocortin Receptor in a Tera-scale vHTS Screen

**Publication Date**: May 8, 2024 - [Pre-print Link](https://chemrxiv.org/engage/chemrxiv/article-details/663aefc321291e5d1db3c68b)

**Target**: Melanocortin Type 2 Receptor (MC2R) - **Design Task**: *De novo* anagonist design using a surrogate model

**Model**: Combinatorial Synthesis Library Variational Auto-Encoder (CSLVAE) - first described [here](https://arxiv.org/abs/2211.04468) (Input: Graph, Output: Query vector to decode into molecule from library)

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: Among the 13/121 with > 50% inhibition at 30 µM, 5 were selected for further assays. 1/5 had EC50 < 10 µM. Therefore 1/121 (0.83%) had affinity < 10 µM

**Outcome**: µM antagonist - **Most Potent Design**: EC50 = 6.7 μM (Table S4)

**Notes**: This work is *generative* in a slightly different sense - the model decodes molecules *from* a dataset and can be seen as a combination of a generative and virtual screening method. 13/121 > 50% inhibition at 30 µM.

------------------------------------------------------------------------------------------------------------

### 28. De novo generation of multi-target compounds using deep generative chemistry

**Publication Date**: May 6, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-47120-y)

**Target**: Dual specificity to MEK1 and mTOR - **Design Task**: *De novo* structure-based design with some fixed moieities (based on known binder)

**Model**: VAE (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement learning - Hill-Climbing

**Hit Rate**: 19/32 (59%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 between 1-10 μM (Fig. 6d)

**Notes**: The 4 most potent compounds achieved > 50% reduction in phosphorlation activity of both MEK1 and mTOR at 1 μM.

------------------------------------------------------------------------------------------------------------

### 29. Synthetically Feasible De Novo Molecular Design of Leads Based on a Reinforcement Learning Model: AI-Assisted Discovery of an Anti-IBD Lead Targeting CXCR4

**Publication Date**: June 12, 2024 - [Paper Link](https://pubs.acs.org/doi/full/10.1021/acs.jmedchem.4c00184)

**Target**: CXCR4 - **Design Task**: *De novo* structure-based antagonist design

**Model**: MLP (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement learning (SAC)

**Hit Rate**: 20/20 (100%)

**Outcome**: nM competitive antagonism with *in vivo* validation - **Most Potent Design**: Antagonistic rate = 78.9 ± 6.2% at 10 nm (*N* = 3 assay replicates) - Table 1

**Notes**: Uses commercially available building blocks and molecular generation follows reaction templates. Uses AutoDock Vina as the docking protocol which is open-source. *In vivo* validation.

------------------------------------------------------------------------------------------------------------
### 30. Accelerated Discovery of Carbamate Cbl-b Inhibitors Using Generative AI Models and Structure-Based Drug Design

**Publication Date**: August 12, 2024 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.4c01034)

**Target**: Cbl-b  - **Design Task**: *De novo* scaffold-based design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES) - Model is [LibINVENT](https://pubs.acs.org/doi/10.1021/acs.jcim.1c00469) which is part of `REINVENT` 

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: N/A (see notes)

**Outcome**: N/A (see notes)

**Notes**: LibINVENT designed 2 molecules which were of interest after FEP validation. Small modifications of these 2 compounds were made and then synthesized. Both were active and the most potent had IC50 1.2 μM. 
A third compound was the result during chiral separation of one of the two synthesized compounds. This third compound was also tested with IC50 37 μM. The insights from these first three compounds inspired the remaining design campaign.

------------------------------------------------------------------------------------------------------------
### 31. Discovery of novel quinoline papain-like protease inhibitors for COVID-19 through topology constrained molecular generative model

**Publication Date**: September 13, 2024 - [Pre-print Link](https://www.biorxiv.org/content/10.1101/2024.09.07.611841v2)

**Target**: Papain-like protease (PLpro)  - **Design Task**: Scaffold hopping

**Model**: GNN with GCN and GGNN blocks (Input: 2D Graph, Output: 2D Graph) - Model is [Tree-Invent](https://pubs.acs.org/doi/10.1021/acs.jcim.3c01626) and generation is autoregressive

**Optimization Algorithm Class**: Reinforcement learning (using REINVENT's loss function)

**Hit Rate**: 9/9 

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 PLpro = 0.0238 µM (Fig. 3b)

**Notes**:  Based on the most potent Tree-Invent molecule (molecule 2 in the paper), a virtual screening library was created with commercial reagents. This library was screened using Glide docking and led to an experimentally validated nM potent compound. *In vivo* validation was achieved.

------------------------------------------------------------------------------------------------------------
### 32. AutoDesigner - Core Design, a De Novo Design Algorithm for Chemical Scaffolds: Application to the Design and Synthesis of Novel Selective Wee1 Inhibitors

**Publication Date**: October 3, 2024 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jcim.4c01031)

**Target**: Wee1 with improved selectivity against PLK1  - **Design Task**: *De novo* scaffold-based design

**Model**: Enumeration

**Optimization Algorithm Class**: Filtering by property values

**Hit Rate**: 3/3 (100%)

**Outcome**: µM inhibitor but with selectivity against PLK1 - **Most Potent Design**: IC50 Wee1 = 58.3 nM and IC50 PLK1 > 10,000 μM (Table 4)

**Notes**: AutoDesigner is *generative* in a slightly different sense, in that it takes libraries of chemical moeities and attaches them, akin to enumeration.
Uses relative free energy perturbation from Schrödinger (FEP+) combined with active learning. 

------------------------------------------------------------------------------------------------------------
### 33. Modern hit-finding with structure-guided de novo design: identification of novel nanomolar A2A receptor ligands using reinforcement learning

**Publication Date**: October 14, 2024 - [Pre-print Link](https://chemrxiv.org/engage/chemrxiv/article-details/6708fba651558a15efc54314)

**Target**: A2A Receptor Antagonist Design - **Design Task**: *De novo* structure-based design

**Model**: GRU RNN (Input: SMILES, Output: SMILES) - Model is `Augmented Hill Climbing (AHC)` which is a modification of `REINVENT` that adds Hill-climbing by backpropagating only on the top 50% best molecules (by reward) per sampled batch

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 8/10 have pKi < 10 μM

**Outcome**: μM antagonist and selective against A2B

**Notes**: Used Glide as the docking software which is proprietary. Through Glide, hydrogen-bond constraints were enforced. For some protein targets, an additional occupancy constraint was enforced. Docking was performed against 7 known A2A structures. Oracle budget was 12,800 which is amongst the most constrained in case studies with experimental validation. 2 co-crystal structures obtained for the most potent ligands.

------------------------------------------------------------------------------------------------------------

### 34. FragGen: Towards 3D Geometry Reliable Fragment-based Molecular Generation

**Publication Date**: March 15, 2024 - [Pre-paper Link](https://arxiv.org/abs/2404.00014), October 16, 2024 - [Paper Link](https://pubs.rsc.org/en/Content/ArticleLanding/2024/SC/D4SC04620J)

**Target**: LTK - **Design Task**: *De novo* design - fragment-based assembly

**Model**: GAT GNN (Input: Geometry, Output: Geometry)

**Optimization Algorithm Class**: Conditional generation (conditioned on protein pocket)

**Hit Rate**: 3/3 (100%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 75.4 nM

------------------------------------------------------------------------------------------------------------

### 35. Target-aware Molecule Generation for Drug Design Using a Chemical Language Model

**Publication Date**: October 29, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-53632-4#Sec2) - February 1, 2024 - [Pre-print Link](https://www.biorxiv.org/content/10.1101/2024.01.08.574635v3)

**Target**: Tuberculosis ClpP - **Design Task**: *De novo* design 

**Model**: Transformer-VAE (Input: Geometry and SMILES, Output: SMILES)

**Optimization Algorithm Class**: Conditional generation

**Hit Rate**: 0/1 (0%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 20.3 μM

**Notes**: Commercially available analogues were tested and were µM potent (IC50). Only 1 generated molecule was directly synthesized.

------------------------------------------------------------------------------------------------------------

### 36. ClickGen: Directed exploration of synthesizable chemical space via modular reactions and reinforcement learning

**Publication Date**: November 22, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-54456-y)

**Target**: PARP1 - **Design Task**: *De novo* design

**Model**: Based on U-Net encoder-decoder architecture (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement Learning and Monte Carlo Tree Search (MCTS)

**Hit Rate**: 2/3 (66%) - 1/3 has a reported IC50 of > 1,000 nM and a concrete measurement was not provided (see Fig. 8)

**Outcome**: µM inhibitor - **Most Potent Designs**: IC50 = 19.24 ± 1.63 nM

**Notes**: Used Schrödinger's computational chemistry software (proprietary) - pharmacophore matching and Glide docking.

------------------------------------------------------------------------------------------------------------

### 37. Discovery of Pyridine-2-Carboxamides Derivatives as Potent and Selective HPK1 Inhibitors for the Treatment of Cancer

**Publication Date**: November 25, 2024 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.4c02421)

**Target**: Hematopoietic progenitor kinase 1 (HPK1) - **Design Task**: Scaffold hopping

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 1/1 (100%)

**Outcome** nM inhibitor - **Most Potent Design**: IC50 = 0.64 nM but moderate selectivity

**Notes**: Chemistry42 generated 1 molecule which performs a scaffold hop on the previously reported [A-745 from AbbVie](https://pubs.acs.org/doi/full/10.1021/acschembio.1c00819). Further SAR optimization led to *in vivo* validation.

**Extended Notes**: There is a series of 3 papers on HPK1 from Insilico Medicine, based on the following [Press Release](https://firstwordpharma.com/story/5922115): 

[1: Target Validation using PandaOmics](https://www.sciencedirect.com/science/article/pii/S022352342400758X?via%3Dihub)

[2: Medicinal Chemistry SAR](https://pubs.acs.org/doi/10.1021/acsmedchemlett.4c00434)

[3: Generative Design with further SAR](https://pubs.acs.org/doi/10.1021/acs.jmedchem.4c02421)

------------------------------------------------------------------------------------------------------------

### 38. Intestinal mucosal barrier repair and immune regulation with an AI-developed gut-restricted PHD inhibitor

**Publication Date**: December 11, 2024 - [Paper Link](https://www.nature.com/articles/s41587-024-02503-w)

**Target**: Hypoxia-inducible factor prolyl hydroxylase (PHD): Both PHD1 and PHD2 - **Design Task**: *De novo* structure-based design by fragment growth of privileged fragment

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: Unclear, the paper states 1 compound was generated and synthesized which was then further SAR optimized. According to this [source](https://www.newswire.ca/news-releases/insilico-medicine-announces-the-nomination-of-two-preclinical-candidates-for-phd2-12-months-after-program-initiation-887323550.html), in total, approximately 115 molecules were synthesized but perhaps some were not directly *generated*.

**Outcome** nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 = 4 nM

**Notes**: The IC50 4 nM compound was generated and then further SAR optimization led to ISM012-042 (improved ADMET). *In vivo* validation was achieved.

------------------------------------------------------------------------------------------------------------

### 39. Generative deep learning enables the discovery of phosphorylation-suppressed STAT3 inhibitors for non-small cell lung cancer therapy

**Publication Date**: - [Paper Link](https://link.springer.com/article/10.1007/s11030-024-11067-5)

**Target**: STAT3 - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES) - same model as used [here](https://www.nature.com/articles/s41467-022-34692-w)

**Optimization Algorithm Class**: Conditional generation

**Hit Rate**: Unclear - paper states 90 generated molecules were selected for synthesis with 2 possessing potent inhibitory activity at 1 μM

**Outcome**: From the paper: "The results demonstrated that HG106 and HG110 significantly suppressed colony formation in all tested NSCLC cell lines at a concentration of 1 μM Fig.4A."
 
**Notes**: Conditional generation resulted in a library of 15,678 generated molecules. Similar to the previous paper where the model was adapted [from](https://www.nature.com/articles/s41467-022-34692-w), the generated library was screened. Oracles include physico-chemical properties, docking (AutoDock 4.0), and MMGBSA.

------------------------------------------------------------------------------------------------------------

### 40. Electron-density informed effective and reliable de novo molecular design and lead optimization with ED2Mol

**Publication Date**: - [Pre-print Link](https://www.biorxiv.org/content/10.1101/2024.12.18.629081v1)

**Target**: 3 Targets: FGFR3 orthosteric inhibitors, CDC42 allosteric inhibitors, and GCK allosteric activator - **Design Task**: *De novo* design and *lead optimization*

**Model**: Uses a VAE and an equivariant GNN (EGNN) (Input: Graph/Geometry, Output: Graph/Geometry) - new model proposed in the paper is named `ED2Mol`

**Optimization Algorithm Class**: Conditional generation

**Hit Rate/Outcome**: 

`FGFR3 Orthosteric Inhibitors`: 50,000 molecules generated, filtered, and clustered. 5 molecules selected (unclear how many synthesized) - $K_D$ = 599 μM. A crystal structure was obtained and informed subsequent lead optimization. The hinge-binding moiety was fixed to generate a 10,000 more molecules and filtered again. 1 molecule selected for synthesis - $K_D$ = 61.4 μM

`CDC42 Allosteric Inhibitors`: 50,000 molecules generated, filtered, and clustered. 2 molecules selected for synthesis - IC50 = 47.58 ± 3.71 μM and 111.63 ± 0.90 μM.

`GCK Allosteric Activator`: Based on a known compound, 10,000 molecules were generated, filtered, and clustered for lead optimization. 2 molecules selected for synthesis - EC50 = 290 nM and 150 nM. Original compound has an EC50 = 1810 nM.

 
**Notes**: One of the relatively few works using electron density to inform the generation of molecules.

------------------------------------------------------------------------------------------------------------

# **2025**

### 41. Discovery of Potent, Highly Selective, and Orally Bioavailable MTA Cooperative PRMT5 Inhibitors with Robust In Vivo Antitumor Activity

**Publication Date**: January 9, 2025 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.4c02732)

**Target**: Protein arginine methyltransferase 5 (PRMT5) - **Design Task**: ligand-based design using fragment growth

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 5/6 (83%) during round-1 generation. 8/8 (100%) during round-2 generation.

**Outcome** nM potent with *in vivo* validation - **Most Potent Design**: MTAP-del viability IC50 = 95 nM

**Notes**: Between round-1 and round-2 generation, some manual SAR was performed. From the most potent generated molecule to the final *in vivo* validated molecule, manual SAR was performed.

------------------------------------------------------------------------------------------------------------

### 42. Designing Macrocyclic Kinase Inhibitors Using Macrocycle Scaffold Hopping with Reinforced Learning (Macro-Hop)

**Publication Date**: March 18, 2025 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.5c00087)

**Target**: PDGFRα kinase - **Design Task**: Shape-based macrocycle scaffold hopping

**Model**: RNN encoder-decoder (Input: SMILES, Output: SMILES) based on [LinkINVENT](https://pubs.rsc.org/en/content/articlelanding/2023/dd/d2dd00115b) - the model in the paper is named `Macro-Hop`

**Optimization Algorithm Class**: Reinforcement learning (uses [REINVENT's](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-017-0235-x) algorithm)

**Hit Rate**: 1/2 (50%)

**Outcome** nM potent - **Most Potent Design**: IC50 = 37.5 nM

**Notes**: The pre-training dataset of macrocycles is available from the authors [here](https://macro-db.dpbio.tech/). The reinforcement learning reward function used OpenEye's OMAGE and ROCS (proprietary software) to compute shape similarity between generated macrocycles and the reference. An initial macrocycle was identified through screening an in-house library. `Macro-Hop` was used to explore scaffold hops of this initial hit.

------------------------------------------------------------------------------------------------------------

### 43. Discovery of Novel SIK2/3 Inhibitors for the Potential Treatment of MEF2C+ Acute Myeloid Leukemia (AML)

**Publication Date**: March 20, 2025 - [Paper Link](https://pubs.acs.org/doi/full/10.1021/acs.jmedchem.4c03225)

**Target**: SIK2/3 - **Design Task**: Structure- and Pharmacophore-based hit optimization

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 3/3 (100%)

**Outcome** nM inhibitor with *in vivo* validation - **Most Potent Designs**: IC50 SIK1 = 85 nM / SIK2 = 7.2 nM / SIK3 =  8.7 nM

**Notes**: This paper describes subsequent efforts building on [previous work](https://www.sciencedirect.com/science/article/pii/S0968089623002626) by the same authors that identified a promising hit molecule with IC50 = 0.023 μM. See Figure 2 - the generation focused on modifying the "solvent" and "P-loop" areas. Pharmacophore templates were extracted from these regions and used to guide generation. Docking performed with Molecular Operating Environment (MOE) software (proprietary)

------------------------------------------------------------------------------------------------------------

### 44. Novel Arbidol derivatives against SARS-CoV-2: a comprehensive approach using computer- and AI-assisted drug design

**Publication Date**: March 27, 2025 - [ACS Spring 2025 Link](https://scimeetings.acs.org/exhibit/Novel-Arbidol-derivatives-against-SARS/4181135)

**Target**: SARS-CoV-2 - **Design Task**: Structure-based design

**Model**: RNN (Input: SMILES, Output: SMILES) - the specific model is named [MegaSyn](https://pubs.acs.org/doi/10.1021/acsomega.2c01404)

**Optimization Algorithm Class**: Reinforcement learning (a variant of hill-climbing - see notes)

**Hit Rate**: Unclear (23 were synthesized but the hit rate is unclear as the pre-print is not released yet)

**Outcome** µM inhibitor with *in vivo* validation - **Most Potent Designs**: EC50 of 0.73 µM against the SARS-CoV-2 omicron variant

**Notes**: This was an oral presentation at ACS Spring 2025. Vanilla [Hill-climbing](https://openreview.net/forum?id=Bk0xiI1Dz) back-propagates with the top X% of sampled molecules based on reward, at a given epoch. The model in this work uses a modified Hill-climbing where the top X% of molecules is **carried** over to the next epoch. If epoch $t+1$ does not generate any better molecules than the previous top X%, then back-propagation occurs again using the same molecules. The authors of [MegaSyn](https://pubs.acs.org/doi/10.1021/acsomega.2c01404) state that the models hyperfocus on specific substructures. Multiple models are trained and results are aggregated to obtain more diverse sets.

------------------------------------------------------------------------------------------------------------

### 45. Discovery of Novel Inhibitors for WD Repeat-Containing Protein 5 (WDR5)-MYC Protein-Protein Interaction

**Publication Date**: May 21, 2025 - [Paper Link](https://onlinelibrary.wiley.com/doi/10.1111/cbdd.70129)

**Target**: WD Repeat-Containing Protein 5 (WDR5)-MYC - **Design Task**: Structure- and ligand-based design

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 

Structure-based approach: 2/3 (66%)* see Notes.

Ligand-based approach: 2/2 (100%)

**Outcome** µM inhibitor - **Most Potent Designs**: IC50 of 1.91 µM (from ligand-based approach)

**Notes**: The same crystal structure information was used as the starting point for structure- and ligand-based design. 

*In the structure-based approach, the paper states that further generation of derivatives of one of the validated generated molecules did not improve activity. 
However, it is unclear how many of these derivatives were made or if they were just not *predicted* to be more potent.

------------------------------------------------------------------------------------------------------------
