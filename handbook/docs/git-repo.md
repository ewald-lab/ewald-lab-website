## Overview

Writing open and reproducible code is an essential part of computational biology research. We adhere to a strict set of organisational and stylistic conventions to maximise code reuse by lab members, improve analysis rigour, and reduce the amount of code clean-up needed before paper submission. These standards are meant for general data analysis repositories that would accompany a publication, not for published software tools.

## Initialising a new repository

Create a new repository within the [Ewald Lab GitHub Org](https://github.com/ewald-lab) with the following specs:

* Use the Ewald Lab analysis repo template
* If it's a project driven primarily by you, the repo name should be YEAR_MONTH_LASTNAME_SHORT_DESCRIPTION, for example 2025_08_Ewald_TimeDynamics
* If it's a large collaborative project, use the name of the collaboration instead of your name, for example 2025_08_OASIS_CellPainting
* Make sure the repository is set to Private; this can be changed to Public after discussion with all team members, or upon publication
* Add the ewald-lab team to the repo as collaborators with 'Write' permissions
* Add the ewald-lab-admin team to the repo as collaborators with 'Admin' permissions (this is just Jess for now)
* Set the license to CC0
* Make sure you include a .gitignore with the type set to the main programming language that you will use (likely Python or R). Add .DS_Store exclusions to the .gitignore
* Populate the README.md in the directory root with a short (few sentences) description of the overall purpose of the project. Over time, explanations of the analysis components will be added to this file.

## Repository structure

Each repository should have one or more 'analysis module' directories in the root. A common set of modules for a simple project could be `00.data_download_exploration/`, `01.analysis_pipeline/`, and `02.downstream_analysis/`. Within each module will be the following sub-directories:

* `inputs/`: any input data files that were retrieved from external sources
* `analysis/`: scripts and notebooks used to process and analyse the data
* `outputs/`: intermediate data and results tables (ie. norm_filtered.parquet or perturbation_stats.csv)
* `figures/`: figures produced by the analysis scripts
* `install_env.sh`: bash script for installing and activating the Python or R environment
* `requirements.txt`: list of dependencies (package name and version) for the environment

Files in the analysis folder should be numbered based on the order in which they should be executed (ie. 00.download_data.py, 01.descripe_exp_design.py, 02.filter_normalize.py, etc). You'll notice that there is a separate environment for each analysis module. This helps keeps environments more lightweight, hopefully reducing dependency conflicts across the entire repository.

## Repository as a lab notebook

If you encounter an issue with the data, an open question that needs discussion, or generate cool results, please describe these in GitHub issues within the repository and tag Jess or other team members instead of sending an email. This keeps a clear record of all project-related troubleshooting, questions, and milestones. This is very helfpul for onboarding new team members to help out with the project, or for reminding ourselves of the reasons why particular decisions were made - this becomes very important for multi-year projects! The only exceptions are discussions that require confidentiality (use email) or quick reminder-type questions (use Slack). Keep in mind that most repositories will be made public eventually, including all associated GitHub Issues, so this is extra motiviation to keep things professional.

## NextFlow

The bulk of your analysis will likely by in the `xx.analysis_pipeline` module. Ideally it will be implemented using [NextFlow](https://www.nextflow.io/). Pipeline orchestration software like NextFlow or Snakemake have a bit of a learning curve, but make running complex pipelines, reproducing them, and experimenting with different parameters or steps much, much, much easier in the long run. We chose NextFlow because this software is officially supported by EBI IT, so there are dedicated training sessions and lots of institutional knowledge on how to make it work well with the EBI cluster.

## General principles

* Only use relative paths (ie. "../inputs/counts.tsv", not "Users/jewald/project_repo/00.data_exploration/inputs/counts.tsv").
* If changing analysis parameters from their default, give them a name and define them at the top of the script or notebook (ie. `corr_threshold = 0.8`).
* Enforce linear progression through modules and through scripts within modules - a module or script should never depend on results produced by a module or script with a higher number. Strictly adhering to this organisation makes it easier for new people (or future you, during paper revisions) to understand what was done.
* Do not read in the same input data multiple times per script - this is usually an indication that you should split the analysis into two parts and start another script.
* Do not mix analysis inputs and outputs - the input folder should be reserved for external inputs. Intermediate results should be written to the outputs folder. Take care to give your outputs sensible names so that it's relatively easy for an outsider to guess the contents of the files.
* Only very small input tables should be committed to the GitHub repo. For larger input files, include a download_XXX.sh file that fetches the data from an online repository or use symlinks to an external storage location on the cluster. If downloading data from online, download to a subdirectory in the inputs dir (ie. inputs/raw_profiles/) and add the subdir to the .gitignore.
* If using Jupyter notebooks, avoid committing printed out dataframes or variables, unless it is a highly meaningful result. For example print(df) is usually not helpful, but print(f"There were {num_sig} significant perturbations") could be a useful reference.
