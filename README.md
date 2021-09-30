# R-notebook-PHBsorting 

Pipelines for data analysis of BarSeq libraries sorted by cell density

### Overview

This repository contains data and analysis pipeline for analysis of a *Cupriavidus necator* (also known as *Ralstonia eutropha*) transposon library grown in nitrogen-rich and nitrogen-starving conditions, and then sorted on a density gradient. The cell density is a proxy for polyhydroxybutyrate (PHB) content, the production of which is induced during nitrogen starvation. 

The sorted library samples have been divided into three fractions: **F1**, **F2** and **F3**. F1 is the lightest fraction, while F3 is the densest fraction. In addition to these, an unsorted **F0** fraction is used as a reference. These fraction samples were prepared using the [BarSeq98](https://doi.org/10.1128/mBio.00306-15) protocol [1] and sequenced on a NextSeq500 system. To calulate fitness scores, the sequencing output was first analyzed using the [ReBar](https://github.com/m-jahn/rebar) pipeline [2]. The output of ReBar is then used as input for the custom analysis scripts in here. The scripts here are based on [BarSeq analysis scripts](https://github.com/m-jahn/R-notebook-ralstonia-proteome) developed by Michael Jahn [3]. Included here is the final output of ReBar, i. e. the files *fitness.Rdata*, *fitness_gene.Rdata*, *result.colsum* and *result.poolcount*. This allows an exploratory analysis of which genes that contribute to increased or decreased PHB production, which can be plotted as the relative abundance in each fraction of strains with a transposon insertation in each gene (presumed to be null mutants for that gene in most cases).  A selection of the intermediary output in the *counts* folder, which was used for diagnostics, is also included. 

The pipeline code is in R notebook format, and can most easily be run and edited in Rstudio. Documentation and tentative conclusions are contained in the notebook file. The data is in either in tsv (tab separated text file) or Rdata format. 

### References 

1. Wetmore et al. 2015 (https://doi.org/10.1128/mBio.00306-15)
1. https://github.com/m-jahn/rebar
1. https://github.com/m-jahn/R-notebook-ralstonia-proteome
