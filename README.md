# BHM-Terrain-Paper
Code for the paper: `A Bayesian hierarchical model to understand the effect of terrain on wind turbine power curves`

## Description: 
This code repository contains the code to reproduce the tables and figures in the paper: A Bayesian hierarchical model to understand the effect of terrain on wind turbine power curves. This document explains the folder structure and provides instruction to execute the code. 

## Software: 
The results are generated using shell scripts (`bash`) that wrap code from `R` software package version `3.6.3` or above and uses the following packages:

- `DSWE`
- `mvtnorm`
- `FNN`
- `optparse`
- `truncdist`
- `latex2exp`

## Folder Structure:

The `root` folder contains the following sub-folders:

- `src`: A folder that contains the core code files.
- `data`: An empty folder. Please put all the data files in this folder. 
- `artifacts`: This folder will store all the model objects during execution and use them generate results.
- `results`: All the results from the paper will be stored in this folder.
- `log`: This folder will contain all the runtime log. If you get any error while running the code, please check the relevant logs in this folder.

## Code Execution:
Each of the tables and figures have their own shell scripts. The following commands can be used to generate each of the results.

  | File       | Command           | # Cores | RAM | Runtime | Output files |
  |------------|-------------------|---------|-----|---------|--------------|
  | Table1.sh | `bash Table1.sh` | 1       | 2GB | 5 minutes| `Table1.txt`|
  | Figure2.sh | `bash Figure2.sh` | 1       | 2GB | 1 minute| `Figure2.png`|
  | Figure3.sh | `bash Figure3.sh` | 1       | 2GB | 1 minute| `Figure3.pdf`|
  | Figure4.sh | `bash Figure4.sh` | 1       | 2GB | 1 minute| `Figure4.pdf`|
  | Figure5.sh | `bash Figure5.sh` | 1       | 2GB | 1 minute| `Figure5.pdf`|
  | Figure7_Table3.sh | `bash Figure7_Table3.sh` | 1       | 2GB | 2 hours | `Figure7a.png` `Figure7b.png` `Table3.txt`|
  | Figure8.sh | `bash Figure8.sh` | 6       | 12GB | 2.5 hours | `Figure8a.pdf` `Figure8b.pdf` `Figure8c.pdf` `Figure8d.pdf` `Figure8e.pdf` `Figure8f.pdf`|
  | Table4_Figure9.sh | `bash Table4_Figure9.sh` | 6       | 12GB | 24 hours | `Figure9a.pdf` `Figure9b.pdf` `Table4.txt`|

**Note:** 

- `Figure8.sh` depends on the results obtained `Figure7_Table3.sh`. Please run `Figure7_Table3.sh` before running `Figure8.sh`.
- We provide a convenient wrapper `Run_All.sh` to execute all the code sequentially. The total runtime is approx 29 hours on `Apple Silicon M1` chip.

## Datasets:

The datasets used in this paper comprises of individual turbine operations data as well as terrain information data. The dataset has not been made public yet. We will update this section when the data is released.
