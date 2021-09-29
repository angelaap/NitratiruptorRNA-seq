# NitratiruptorRNA-seq
This repository includes the generated code for Nitratiruptor transcriptome analysis under metal stress (i.e. Cd, Cu) and intermediate files created. 

## From raw fasta files to transcript counts

FASTA files were processed using the Nextflow pipeline nfcore/rnaseq (version 3.1, https://nf-co.re/rnaseq#introduction) mainly with standard settings. Nf-core is a a community effort to collect a curated set of analysis pipelines built using Nextflow (a workflow tool to run tasks across multiple compute infrastructures in a very portable manner).

Nextflow moduke was already prepared by the OIST Bioinformatic User group (refer here https://github.com/oist/BioinfoUgrp)making nf-core pipeline available to the users.


DESeq and enrichment analysis details: https://github.com/angelaap/NitratiruptorRNA-seq/blob/main/NitratiruptorRNA-seq.Rmd
