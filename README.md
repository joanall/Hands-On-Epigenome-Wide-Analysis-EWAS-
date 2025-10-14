# **Hands-On-Epigenome-Wide-Analysis-EWASl** 

**Joana Llauradó**, Predoctoral Researcher at the Barcelona Institute for Global Health (ISGlobal).  
**Mariona Bustamante**,  Senior Research Scientist at the Barcelona Institute for Global Health (ISGlobal).  


**Description:** 
This hands-on exercise focuses on the analysis phase of an Epigenome-Wide Association Study (EWAS). 
Using preprocessed DNA methylation data, participants will learn how to identify associations between 
an environmental exposure—such as smoking—and methylation levels across the genome.

The data quality control (QC) step will not be assessed in this session. However, participants 
can explore QC independently using the example code provided [here: insert link], which demonstrates h
ow to perform standard preprocessing and QC steps.

During this practical, we will perform EWAS analysis and basic downstream interpretation to gain 
biological insight from the results. Participants will learn how to run association models, 
correct for multiple testing, visualize significant findings (e.g., using Manhattan and QQ plots), 
and interpret the top CpG sites and enriched pathways related to the exposure of interest.

**Considerations**: Public data from [link] It must be noted that this data is public and has been
revied/selcetd to be able tor un this nalaysis in a short period of time. 
Ewas data usually is upt to XXXX GB and a compute with enough memory or clsuter is nneded
to run this nalaysis. Also the time needed is higher than the one for this Hands-on. 

# Repository Guide 

The repository contains the following documents: 

* **ewas_tutorial.ipynb:** Notebok for the practial ttotrial with the code needed to perfom EWAS
* **data:** Folder with the data that will be sued during the session. 

# **Reminder: Introduction to NoteBook**

This tutorial **[ewas_tutoial.ipnyb](https://github.com/joanall/Hands-On-Epigenome-Wide-Analysis-EWAS-/blob/main/ewas_tutorial.ipynb)**
file is a Notebook object. you will be guided step by step from loading a dataset to performing analysis.

**To access the tutorial:**

- **Open** the exposome_tutorial.ipynb file.

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





