# BIOC3301 - Analysis of change in concentration of core phyla in Gordon Square Gardens over time

## Info
This is a repository of the scripts and files use for the project titled "Analysis of change in concentration of core phyla in Gordon Square Gardens over time". These scripts were performed using QIIME version 1.9.1 on EPCC’s Cirrus supercomputer for the analysis of 16S V4 rRNA of soil samples collected from Gordon Square Gardens, London.

## Script Workflow
* joinends.pbs - join the paired ends and demultiplex data
* pickotus.pbs - pick operational taxonomic units (OTUs) using the closed referencing method from the Greengenes database
* removesamples.pbs - remove non-park samples from 10/18
* corebiome.pbs - generates a core microbiome for 01/16, 02/17 and 10/18 from 50% - 100% abundance
* merge.pbs - merge 95% core biom tables and mapping files from 01/16 02/17 and 10/18 samples
* heatmap.pbs - generates heatmap of OTUs from 95% abundance merged core microbiome 
* cda.pbs - performs corde diversity analysis of 95% abundance merged core microbiome 
* groupsig.pbs - performs Kruskal-Wallis test for group significance on 95% abundance merged core microbiome 

## Output Files
* kw2.txt - Kruskal-Wallis group significance test of 95% abundance merged core microbiome
* heatmap2.pdf - PDF file - heatmap of OTUs from 95% abundance merged core microbiome 
* heatmap2.png - PNG file - heatmap of OTUs from 95% abundance merged core microbiome 
