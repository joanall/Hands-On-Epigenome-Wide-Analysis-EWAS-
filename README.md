# **Hands-On-Epigenome-Wide-Analysis-EWAS** 

**Joana Llauradó**, Predoctoral Researcher at the Barcelona Institute for Global Health (ISGlobal).  
**Mariona Bustamante**,  Senior Research Scientist at the Barcelona Institute for Global Health (ISGlobal).  


**Description:** 
This hands-on exercise is to perfrom an Epigenome-Wide Association Study (EWAS). 
Using preprocessed DNA methylation data, participants will learn how to identify associations between 
an environmental exposure — such as smoking — and methylation levels across the genome.

The data quality control (QC) step will not be covered in this session (it usually includes sample and probe
filtering, normalisation, winsorisation, batch-effect checks, etc.). Participants can explore QC
independently using the example code provided in https://github.com/epicenteredresearch/PACEanalysis/tree/main
and https://github.com/isglobal-brge/course_methylation, which demonstrate how to perform standard
preprocessing and QC steps.

During this practical, we will perform EWAS analysis and basic downstream interpretation to gain 
biological insight from the results. Participants will learn how to run association models, 
correct for multiple testing, visualize significant findings (e.g., using Manhattan and QQ plots), 
and interpret the top CpG sites and enriched pathways related to the exposure of interest.

**Data**: Public data from the GEO study [GSE42861](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE42861)
(Liu et al., *Nat Biotechnol* 2013, PMID: [23334450](https://pubmed.ncbi.nlm.nih.gov/23334450/)): a rheumatoid
arthritis case–control study with blood DNA methylation measured with the Illumina 450K array. In this tutorial we use
**smoking** (current vs never) as the exposure. We use a pre-processed subset (cohort 1, 294 participants) with a reduced number of CpGs.

**Considerations**: This data is public and has been reduced/selected so that the analysis can be run in a short
period of time. Real EWAS data are much larger (raw IDAT files take roughly 10–20 MB per sample on the 450K array,
i.e. several to tens of GB for a full study), and a computer with enough memory or a computing cluster is needed to
run the analysis. The time needed is also much longer than the time available in this hands-on session.

**Main R packages**: [`meffil`](https://github.com/perishky/meffil) (pre-processing and EWAS of Illumina methylation
arrays), `Biobase` (ExpressionSet objects), `tableone` (descriptives), `qqman` and `ggplot2` (QQ, Manhattan and
volcano plots), `IlluminaHumanMethylation450kanno.ilmn12.hg19` (CpG annotation), and `clusterProfiler`, `ReactomePA`
and `org.Hs.eg.db` (GO, KEGG and Reactome enrichment). See Section 1 of the notebook for details.

**Contents**: data loading and descriptives, EWAS with robust linear regression, genomic inflation (λ),
significance thresholds (FDR, suggestive, Bonferroni, permutation-based), volcano and Manhattan plots, CpG annotation,
enrichment analyses (GO, Reactome, KEGG), online tools (eFORGE, Enrichr, EWAS Catalog) and an introduction to
epigenetic clocks.

**Based on/adapted from**: Summer School in Global Health 2023 – EWAS course,
https://github.com/isglobal-brge/course_methylation, where you can find more material.

# Repository Guide 

The repository contains the following documents: 

* **ewas_tutorial.ipynb:** Notebook for the practical tutorial with the code needed to perform the EWAS.
* **data:** Folder with the data that will be used during the session (methylation data and 450K annotation).
* **results:** Pre-computed results and plots, in case any step cannot be run during the session.
* **setup:** `build_colab_library.ipynb`, for instructors: installs all the packages once in Colab and saves a copy of the R library, which the tutorial downloads (published as a GitHub release, tag `colab-lib`).

# **Reminder: Introduction to NoteBook**

This tutorial **[ewas_tutorial.ipynb](https://github.com/joanall/Hands-On-Epigenome-Wide-Analysis-EWAS-/blob/main/ewas_tutorial.ipynb)**
file is a Notebook object. you will be guided step by step from loading a dataset to performing analysis.

**To access the tutorial:**

- **Open** the ewas_tutorial.ipynb file.

- **Click** the “Open in Colab” button at the top of the notebook.

**You’ll need to sign in with a Google account to run the Colab tutorial.**

The *Jupyter* (Python) notebook is an approach that combines text blocks (like this one)
together with code blocks or cells. The great advantage of this type of cell is its interactivity, 
as they can be executed to check the results directly within them. 
*Very important:* **the order of instructions is fundamental**, so each cell in this notebook 
must be executed sequentially. If any are omitted, the program may throw an error, so you should 
start from the beginning if in doubt.

First of all:

Once inside google colab, it is **very very important** that at the start you select 
**"*Open in draft mode*" (draft mode)**, at the top left. Otherwise, it will not allow you to 
execute any code block, for security reasons. When the first of the blocks is executed, 
the following message will appear: "*Warning: This notebook was not created by Google.*". 
Do not worry, you should trust the content of the notebook (*NoteBook*) and click "Run anyway".

Let’s go!

Click the "play" button on the left side of each code cell. Lines of code that begin
with a hashtag (#) are comments and do not affect the execution of the program.

You can also click on each cell and press "*ctrl+enter*" (*cmd+enter* on Mac).

Each time you run a block, you will see the output just below it. Th
e information is usually always related to the last instruction, along with all 
the `print()` commands in the code.





