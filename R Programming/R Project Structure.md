--------------------------------------------------------------------------
# Directories
R has a powerful notion of the *working directory*. This is where R looks for files that
you ask it to load and where it will put any files that you ask it to save.

You can print this out in R code by running **getwd()**
`getwd()
`#> [1] "/Users/hadley/Documents/r4ds"`

You can set the working directory from within R, but we do not recommend it:
`setwd("/path/to/my/CoolProject")`
There’s a better way—a way that also puts you on the path to managing your R work
like an expert. That way is the RStudio project.

# Projects
Projects are a way to organize input data, R scripts, analytical results, and figures together in one single directory. R Projects help us do just that.

#### Creating a project
Select File > New Project to create a new project directory within RStudio.

#### Reopening a project
After writing the scripts and performing the analysis, you can save the figures and visuals as png files in the directory, and after quitting RStudio you will notice a "**.Rproj**" file. You can double click the .Rproj file to reopen the project again on RStudio.

#### Relative paths
Once you’re inside a project, you should only ever use relative paths, not absolute paths. 

# Project structure and files

#### Here's a good way of naming and organizing the same set of files:
01-load-data.R
02-exploratory-analysis.R
03-model-approach-1.R
04-model-approach-2.R
fig-01.png
fig-02.png
report-2022-03-20.qmd
report-2022-04-02.qmd
report-draft-notes.txt

It consists of various script files with the .R extension, which do the work of loading the data, exploratory analysis, and modelling. The script files have been numbered in the order they were executed, and have a consistent naming scheme.  

Some output figures which have been saved as png images. Report files and text notes. 

#### Guide to naming files
1. Filenames should be machine readable: avoid spaces, symbols, and special char‐
acters. Don’t rely on case sensitivity to distinguish files.
2. Filenames should be human readable: use filenames to describe what’s in the file.
3. Filenames should play well with default ordering: start filenames with numbers
so that alphabetical sorting puts them in the order they get used.