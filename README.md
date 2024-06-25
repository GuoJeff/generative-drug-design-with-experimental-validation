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

**Fun fact (as of June 25, 2024)**: 22/46 examples are from 2024!

<br>

**Every entry contains the following information:**
1. Publication Date - Paper Link
2. Target - Design Task
3. Model (Input: [Molecular Representation], Output: [Molecular Representation])
4. Hit Rate (Number of synthesized examples with IC50 < 10µM or EC50 < 10µM) - **NOTE**: Designs that underwent manual domain-expert modifications are excluded
5. Outcome (denoted nM if < 10 nM) - Most Potent Design (**NOTE**: Most potent *without* any domain-expert modifications. This is in contrast to our [Review Paper](https://rdcu.be/dLah8) which reports the **final** outcome)
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

# **2021**

### 3. A Novel Scalarized Scaffold Hopping Algorithm with Graph-Based Variational Autoencoder for Discovery of JAK1 Inhibitors

**Publication Date**: August 24, 2021 - [Paper Link](https://pubs.acs.org/doi/10.1021/acsomega.1c03613)

**Target**: JAK1 - **Design Task**: Scaffold hopping

**Model**: GraphGMVAE (Input: Graph, Output: SMILES)

**Hit Rate**: 7/7 (100%)

**Outcome** nM inhibitor - **Most Potent Design**: IC50 =  5.0 nM

**Notes**: The reference compound for scaffold hopping has an IC50 of 45 nM

------------------------------------------------------------------------------------------------------------

### 4. Combining generative artificial intelligence and on-chip synthesis for de novo drug design

**Publication Date**: June 11, 2021 - [Paper Link](https://www.science.org/doi/10.1126/sciadv.abg3338)

**Target**: LXR - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 17/25 (68%)

**Outcome** µM agonist - **Most Potent Design**: EC50 LXRα = 0.21 ± 0.02 µM (*N* = 3 assay replicates)

**Notes**: Used "microfluidics platform for on-chip chemical synthesis"

------------------------------------------------------------------------------------------------------------

### 5. Beam Search for Automated Design and Scoring of Novel ROR Ligands with Machine Intelligence

**Publication Date**: June 24, 2021 - [Paper Link](https://onlinelibrary.wiley.com/doi/full/10.1002/anie.202104405)

**Target**: RORγ - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 3/3 (100%)

**Outcome** µM agonist - **Most Potent Design**: IC50 LXRα = 0.37 ± 0.05 µM (*N* = at least 4 assay replicates)

------------------------------------------------------------------------------------------------------------

# **2022**

### 6. Discovery of Pyrazolo[3,4-d]pyridazinone Derivatives as Selective DDR1 Inhibitors via Deep Learning Based Design, Synthesis, and Biological Evaluation

**Publication Date**: January 13, 2022 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.1c01205)

**Target**: DDR1 - **Design Task**: *De novo* scaffold-based decoration

**Model**: BiRNN encoder–decoder (Input: SMILES, Output: SMILES)

**Hit Rate**: 2/2 (100%)

**Outcome**: nM (borderline µM) inhibitor - **Most Potent Design**: IC50 = 10.2 ± 1.2 nM

**Notes**: The generated set was virtually screened and 2 compounds with the highest docking scores were synthesized. The authors further performed SAR studies.

------------------------------------------------------------------------------------------------------------

### 7. Effective Reaction-Based De Novo Strategy for Kinase Targets: A Case Study on MERTK Inhibitors

**Publication Date**: March 30, 2022 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jcim.2c00068)

**Target**: MERTK - **Design Task**: Reaction based *de novo* design

**Model**: GRU RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 15/17 (100%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 53.4 nM

**Notes**: RNN model generates building blocks compatible with selected reactions.

------------------------------------------------------------------------------------------------------------

### 8. Recurrent neural network (RNN) model accelerates the development of antibacterial metronidazole derivatives

**Publication Date**: August 15, 2022 - [Paper Link](https://pubs.rsc.org/en/content/articlelanding/2022/ra/d2ra01807a)

**Target**: Bacteria - **Design Task**: *De novo* design

**Model**: GRU RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 0/1 (0%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 *S. aureus* = 28.21 µM

**Notes**: 1 generated compound and 11 of its derivatives were synthesized. Within the 11 derivatives, 2 had IC50 < 10 μM. There were additional actives with a concrete potency measured > 10 μM.

------------------------------------------------------------------------------------------------------------

### 9. Target-Focused Library Design by Pocket-Applied Computer Vision and Fragment Deep Generative Linking

**Publication Date**: October 18, 2022 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.2c00931)

**Target**: CDK8 - **Design Task**: Fragment linking

**Model**: GGNN GNN (Input: Graph, Output: Graph)

**Hit Rate**: 9/43 (21%)

**Outcome**: nM inhibitor - **Most Potent Design**: IC50 = 6.4 nM (*N* = 3 assay replicates)

**Notes**: 2 rounds of generation. First round = 37 synthesized, second round = 6 synthesized. Second round takes the optimal inhibitor found from the first round and generates more linkers.

------------------------------------------------------------------------------------------------------------

### 10. PCW-A1001, AI-assisted de novo design approach to design a selective inhibitor for FLT-3(D835Y) in acute myeloid leukemia

**Publication Date**: November 25, 2022 - [Paper Link](https://www.frontiersin.org/articles/10.3389/fmolb.2022.1072028/full)

**Target**: FLT-3 - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 1/1 (100%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 764 nM

------------------------------------------------------------------------------------------------------------

# **2023**

### 11. Leveraging molecular structure and bioactivity with chemical language models for de novo drug design

**Publication Date**: January 7, 2023 - [Paper Link](https://www.nature.com/articles/s41467-022-35692-6)

**Target**: PI3Kγ - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 3/18 (17%)

**Outcome**: µM inhibitor - **Most Potent Design**: Kd = 63 nM (*N* = 2 assay replicates)

**Notes**: 16 molecules (not the top scoring) were purchased from commercial suppliers resulting in a Kd = 640 nM hit. 2 top scoring compounds were manually synthesized and the most potent design had Kd = 63 nM. Derivatives of the top scoring generated compounds were also synthesized resulting in a compound with IC50 = 6.5 nM.

------------------------------------------------------------------------------------------------------------

### 12. Application of deep generative model for design of Pyrrolo[2,3-d] pyrimidine derivatives as new selective TANK binding kinase 1 (TBK1) inhibitors

**Publication Date**: February 5, 2023 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0223523422009369?via%3Dihub)

**Target**: TBK1 - **Design Task**: Fragment linking

**Model**: Transformer (Input: SMILES, Output: SMILES)

**Hit Rate**: 1/1 (100%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 66.7 nM (*N* = 2 assay replicates)

**Notes**: 1 generated molecule was synthesized with IC50 = 66.7 nM. Further SAR studies resulted in more potent designs.

------------------------------------------------------------------------------------------------------------

### 13. Accelerated Discovery of Macrocyclic CDK2 Inhibitor QR-6401 by Generative Models and Structure-Based Drug Design

**Publication Date**: February 8, 2023 - [Paper Link](https://pubs.acs.org/doi/10.1021/acsmedchemlett.2c00515)

**Target**: CDK2 - **Design Task**: Fragment hopping/linking

**Model**: VAE and transformer (Input: SMILES, Output: SMILES)

**Hit Rate**: 17/23 (74%)

**Outcome**: nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 CDK2/E1 = 0.37 nM

**Notes**: The hit rate is not completely accurate as the authors state some modifications were made on the generated structures for synthesis ease (it is unclear the extent of this). 13 compounds were initially synthesized. The crystal structure for one compound was solved and then a second generation campaign to generate linkers to form **macrocycles** was performed. The final optimal compound was validated ***in vivo***.

------------------------------------------------------------------------------------------------------------

### 14. De Novo Design of Nurr1 Agonists via Fragment-Augmented Generative Deep Learning in Low-Data Regime

**Publication Date**: May 31, 2023 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.3c00485)

**Target**: Nurr1 - **Design Task**: *De novo* design

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

**Hit Rate**: 2/6 (33%)

**Outcome**: µM agonist - **Most Potent Design**: EC50 = 0.07 µM

**Notes**: The model was fine-tuned with 1 known Nurr1 agonist which has an EC50 = 0.4 µM.

------------------------------------------------------------------------------------------------------------

# **2024**

### 15. Prospective de novo drug design with deep interactome learning

**Publication Date**: April 22, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-47613-w)

**Target**: PPARγ - **Design Task**: *De novo* design

**Model**: Graph transformer-LSTM RNN (Input: Graph, Output: SMILES)

**Hit Rate**: 2/6 (33%)

**Outcome**: µM agonist - **Most Potent Design**: PPARγ EC50 = 1.5 ± 0.2 µM and PPARδ EC50 = 0.24 ± 0.05 µM
 
**Notes**: The model was fine-tuned with 1 known Nurr1 agonist which has an EC50 = 0.4 µM.

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

**Model**: LSTM RNN (Input: SMILES, Output: SMILES)

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

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 0.023 μM

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

**Outcome**: μM inhibitor with *in vivo* validation - **Most Potent Design**: Quoted from paper: "EC50 0.4 μM against A/St. Petersburg/63/2020, 0.29 μM against A/Vladivostok/2/2009, and 0.74 μM against B/Samara/32/2018 strains (Fig. 4A)"

**Notes**: *in vivo* validation was demonstrated.

------------------------------------------------------------------------------------------------------------

### 14. Target-aware Molecule Generation for Drug Design Using a Chemical Language Model

**Publication Date**: February 1, 2024 - [Pre-print Link](https://www.biorxiv.org/content/10.1101/2024.01.08.574635v3)

**Target**: Tuberculosis ClpP - **Design Task**: *De novo* design 

**Model**: Transformer-VAE (Input: Geometry and SMILES, Output: SMILES)

**Optimization Algorithm Class**: Conditional generation

**Hit Rate**: 0/1 (0%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 39.8 μM

**Notes**: Commercially available analogues were tested and were µM potent (IC50). Only 1 generated molecule was directly synthesized.

------------------------------------------------------------------------------------------------------------

### 15. Quantum Computing-Enhanced Algorithm Unveils Novel Inhibitors for KRAS

**Publication Date**: February 13, 2024 - [Pre-print Link](https://arxiv.org/abs/2402.08210)

**Target**: KRAS - **Design Task**: *De novo* structure-based design 

**Model**: Quantum Computer-LSTM RNN (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Classical optimizer

**Hit Rate**: 1/12 (8%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 1.4 μM

**Notes**: First example of a quantum computer application with experimental validation. There were also additional actives with a concrete measured potency > 10 µM.

------------------------------------------------------------------------------------------------------------

### 16. Generate What You Can Make: Achieving in-house synthesizability with readily available resources in de novo drug design

**Publication Date**: March 5, 2024 - [Pre-print Link](https://chemrxiv.org/engage/chemrxiv/article-details/65e51a8466c138172921935f)

**Target**: MGLL - **Design Task**: *De novo* design with an activity model

**Model**: Graph transformer (Input: Graph, Output: Graph)

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 1/3 (33%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 1 μM

**Notes**: Generation using in-house collection of building blocks.

------------------------------------------------------------------------------------------------------------

### 17. A small-molecule TNIK inhibitor targets fibrosis in preclinical and clinical models

**Publication Date**: March 8, 2024 - [Paper Link](https://www.nature.com/articles/s41587-024-02143-0) - [Blog Post](https://insilico.com/blog/first_phase2)

**Target**: TNIK - **Design Task**: *De novo* structure-based design

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: Unknown

**Outcome**: nM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 = 4.8 nM

**Notes**: Initial generation led to a nM potent compound but with poor ADMET properties resulting in high clearance in human and mice liver microsomes. Lead optimization led to improved ADMET properties and ultimately *in vivo* validation. 

***Notably, Phase 1 clinical trial results were reported and this molecule is the first generative design to progress to phase 2 clinical trials.***

------------------------------------------------------------------------------------------------------------

### 18. Accelerating factor Xa inhibitor discovery with a de novo drug design pipeline

**Publication Date**: March 11, 2024 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0968089624000762?via%3Dihub)

**Target**: Factor Xa - **Design Task**: Scaffold-based

**Model**: Attention-convolution layers (Input: Substructure vector, Output: SMILES)

**Optimization Algorithm Class**: Mixed-Integer NonLinear Programming from this [Paper](https://aiche.onlinelibrary.wiley.com/doi/full/10.1002/aic.17748)

**Hit Rate**: Unknown (see Notes)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 34.57 μM

**Notes**: 8 commercially available generated molecules were purchased. Only the most potent affinity was reported.

------------------------------------------------------------------------------------------------------------

### 19. PocketFlow is a data-and-knowledge-driven structure-based molecular generative model

**Publication Date**: March 11, 2024 - [Paper Link](https://www.nature.com/articles/s42256-024-00808-8)

**Target**: HAT1 and YTHDC1 - **Design Task**: *De novo* design

**Model**: Flow (Input: Geometry, Output: Geometry)

**Optimization Algorithm Class**: Conditional generation (conditioned on protein pocket)

**Hit Rate**: 0/2 (0%) and 0/3 (0%)

**Outcome**: µM inhibitors - **Most Potent Design**: For HAT1: IC50 = 72.36 ± 8.03 μM and for YTHDC1: IC50 = 32.60 ± 2.72 μM (*N* = 3 assay replicates)

**Notes**: There were also additional actives with a concrete measured potency > 10 µM.

------------------------------------------------------------------------------------------------------------

### 20. Deep Geometry Handling and Fragment-wise Molecular 3D Graph Generation

**Publication Date**: March 15, 2024 - [Pre-paper Link](https://arxiv.org/abs/2404.00014)

**Target**: LTK - **Design Task**: *De novo* design - fragment-based assembly

**Model**: GAT GNN (Input: Geometry, Output: Geometry)

**Optimization Algorithm Class**: Conditional generation (conditioned on protein pocket)

**Hit Rate**: 3/3 (100%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 = 75.4 nM

------------------------------------------------------------------------------------------------------------

### 21. Generative AI for designing and validating easily synthesizable and structurally novel antibiotics

**Publication Date**: March 22, 2024 - [Paper Link](https://www.nature.com/articles/s42256-024-00809-7)

**Target**: Bacteria - **Design Task**: *De novo* design with an activity model

**Model**: Monte Carlo Tree Search (MCTS) (Input: Variable, Output: Variable). The activity model takes variable input/output.

**Optimization Algorithm Class**: Monte Carlo Tree Search (MCTS)

**Hit Rate**: 6/58 (10%) - 70 generated molecules were ordered from Enamine and 58 were successfully syntehsized with purity > 90% in ~4 weeks time.

**Outcome**: µM inhibitor with *in vivo* validation. 6 were bioactive against *A. baumannii ATCC 19606R* - **Most Potent Designs**: MIC ≤ 8 µg ml−1

**Notes**: Enforced chemical reactions as permitted transformations during generation.

------------------------------------------------------------------------------------------------------------

### 22. Abstract 5727: ISM9682A, a novel and potent KIF18A inhibitor, shows robust antitumor effects against chromosomally unstable cancers

**Publication Date**: March 22, 2024 - [Paper Link](https://aacrjournals.org/cancerres/article/84/6_Supplement/5727/741278/Abstract-5727-ISM9682A-a-novel-and-potent-KIF18A)

**Target**: KIF18A - **Design Task**: *De novo* structure-based design

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: Unknown (see Notes)

**Outcome**: *in vivo* validation.

**Notes**: 110 molecules were synthesized and tested - [Source](https://www.genengnews.com/topics/artificial-intelligence/insilico-joins-scramble-to-treat-solid-tumors-by-targeting-kif18a/).

------------------------------------------------------------------------------------------------------------

### 23. A dual diffusion model enables 3D molecule generation and lead optimization based on target pockets

**Publication Date**: March 26, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-46569-1)

**Target**: CDK2 - **Design Task**: *Lead optimization*

**Model**: Diffusion (Input: Geometry, Output: Geometry)

**Optimization Algorithm Class**: Conditional generation (conditioned on protein pocket)

**Hit Rate**: 7/7

**Outcome**: nM inhibitor - **Most Potent Design**: IC50 CDK2/E1 = 0.090 nM

**Notes**: Original reference compound has an IC50 CDK2/E1 = 8.1 nM. 2 rounds of generation: 4 molecules synthesized from round 1 resulting in the most potent design IC50 CDK2/E1 = 0.253 nM. 
The second round of focused on intra-linking the molecules resulting in macrocycles. 3 were synthesized and the final most potent design IC50 CDK2/E1 = 0.090 nM.

------------------------------------------------------------------------------------------------------------

### 24. Discovery of 3-hydroxymethyl-azetidine derivatives as potent polymerase theta inhibitors

**Publication Date**: April 1, 2024 - [Paper Link](https://www.sciencedirect.com/science/article/pii/S0968089624000762?via%3Dihub)

**Target**: Polθ - **Design Task**: Fragment linking

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 4/6 (33%)

**Outcome**: µM inhibitor with *in vivo* validation - **Most Potent Design**: IC50 = 126.1 μM

**Notes**: Further SAR studies ultimately led to *in vivo* validation.

------------------------------------------------------------------------------------------------------------

### 25. Quantum-assisted fragment-based automated structure generator (QFASG) for small molecule design: an in vitro study

**Publication Date**: April 3, 2024 - [Paper Link](https://www.frontiersin.org/articles/10.3389/fchem.2024.1382512/full)

**Target**: CAMKK2 and ATM - **Design Task**: Fragment linking

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: 2/3 (66%) and 1/3 (33%)

**Outcome**: µM inhibitors - **Most Potent Design**: For CAMKK2: IC50 = 3 μM and for ATM: IC50 = 4 μM

------------------------------------------------------------------------------------------------------------

### 26. Discovery of a Novel and Potent Cyclin-Dependent Kinase 8/19 (CDK8/19) Inhibitor for the Treatment of Cancer

**Publication Date**: May 1, 2024 - [Paper Link](https://pubs.acs.org/doi/10.1021/acs.jmedchem.4c00248)

**Target**: CDK8/19 - **Design Task**: *De novo* structure-based design with some fixed moieities (based on known binder)

**Model**: Chemistry42 (Input: Mixed, Output: Mixed). Mixed = SMILES, fingerprints, graphs

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: N/A (see Notes)

**Outcome**: N/A (see Notes)

**Notes**: Compounds were manually designed based on generated molecules and 12 total compounds were synthesized. 
In the end, *in vitro* studies using murine CDX model for human mantle cell lymphoma showed IC50 = 1.34 nm. *In vivo* validation was achieved.

------------------------------------------------------------------------------------------------------------

### 27. Generative Active Learning For The Search of Small-molecule Protein Binders 

**Publication Date**: May 2, 2024 - [Pre-print Link](https://arxiv.org/abs/2405.01616)

**Target**: CDK8/19 - **Design Task**: *De novo* structure-based design with some fixed moieities (based on known binder)

**Model**: MPNN GNN (Input: Graph, Output: Graph)

**Optimization Algorithm Class**: Reinforcement learning (PPO)

**Hit Rate**: N/A (see Notes)

**Outcome**: N/A (see Notes)

**Notes**: 35 analogues of the generated molecules were synthesized. 23/35 have IC50 < 10 μM. The most potent design has IC50 = 0.43 μM.

------------------------------------------------------------------------------------------------------------

### 28. NGT: Generative AI with Synthesizability Guarantees Identifies Potent Inhibitors for a G-protein Associated Melanocortin Receptor in a Tera-scale vHTS Screen

**Publication Date**: May 8, 2024 - [Pre-print Link](https://chemrxiv.org/engage/chemrxiv/article-details/663aefc321291e5d1db3c68b)

**Target**: Melanocortin Type 2 Receptor (MC2R) - **Design Task**: *De novo* anagonist design using a surrogate model

**Model**: Combinatorial Synthesis Library Variational Auto-Encoder (CSLVAE) - first described [here](https://arxiv.org/abs/2211.04468) (Input: Graph, Output: Query vector to decode into molecule from library)

**Optimization Algorithm Class**: Reinforcement learning

**Hit Rate**: Among the 13/121 with > 50% inhibition at 30 µM, 5 were selected for further assays. 1/5 had EC50 < 10 µM. Therefore 1/121 (0.83%) had affinity < 10 µM

**Outcome**: µM antagonist - **Most Potent Design**: EC50 = 6.7 μM (Table S4)

**Notes**: This work is *generative* in a slightly different sense - the model decodes molecules *from* a dataset and can be seen as a combination of a generative and virtual screening method. 13/121 > 50% inhibition at 30 µM.

------------------------------------------------------------------------------------------------------------

### 29. De novo generation of multi-target compounds using deep generative chemistry

**Publication Date**: May 6, 2024 - [Paper Link](https://www.nature.com/articles/s41467-024-47120-y)

**Target**: Dual specificity to MEK1 and mTOR - **Design Task**: *De novo* structure-based design with some fixed moieities (based on known binder)

**Model**: VAE (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement learning (PPO)

**Hit Rate**: 19/32 (59%)

**Outcome**: µM inhibitor - **Most Potent Design**: IC50 between 1-10 μM (Fig. 6d)

**Notes**: The 4 most potent compounds achieved > 50% reduction in phosphorlation activity of both MEK1 and mTOR at 1 μM.

------------------------------------------------------------------------------------------------------------

### 30. Synthetically Feasible De Novo Molecular Design of Leads Based on a Reinforcement Learning Model: AI-Assisted Discovery of an Anti-IBD Lead Targeting CXCR4

**Publication Date**: June 12, 2024 - [Paper Link](https://pubs.acs.org/doi/full/10.1021/acs.jmedchem.4c00184)

**Target**: CXCR4 - **Design Task**: *De novo* structure-based antagonist design

**Model**: MLP (Input: SMILES, Output: SMILES)

**Optimization Algorithm Class**: Reinforcement learning (SAC)

**Hit Rate**: 20/20 (100%)

**Outcome**: nM competitive antagonism with *in vivo* validation - **Most Potent Design**: Antagonistic rate = 78.9 ± 6.2% at 10 nm (*N* = 3 assay replicates) - Table 1

**Notes**: Uses commercially available building blocks and molecular generation follows reaction templates. Uses AutoDock Vina as the docking protocol which is open-source. *In vivo* validation.

------------------------------------------------------------------------------------------------------------

### 31. AutoDesigner - Core Design, a De Novo Design Algorithm for Chemical Scaffolds: Application to the Design and Synthesis of Novel Selective Wee1 Inhibitors

**Publication Date**: June 14, 2024 - [Pre-print Link](https://chemrxiv.org/engage/chemrxiv/article-details/666b21905101a2ffa883d62c)

**Target**: Wee1 with improved selectivity against PLK1  - **Design Task**: *De novo* scaffold-based design

**Model**: Enumeration

**Optimization Algorithm Class**: Filtering by property values

**Hit Rate**: 3/3 (100%)

**Outcome**: µM inhibitor but with selectivity against PLK1 - **Most Potent Design**: IC50 Wee1 = 53.8 μM and IC50 PLK1 > 10,000 μM (Table 4)

**Notes**: AutoDesigner is *generative* in a slightly different sense, in that it takes libraries of chemical moeities and attaches them, akin to enumeration.
Uses relative free energy perturbation from Schrödinger (FEP+) combined with active learning. 

------------------------------------------------------------------------------------------------------------


