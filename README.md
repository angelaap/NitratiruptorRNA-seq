# NitratiruptorRNA-seq
This repository includes the generated code for Nitratiruptor transcriptome analysis under metal stress (i.e. Cd, Cu) and intermediate files created. 

## From raw fasta files to transcript counts

FASTA files were processed using the Nextflow [nfcore/rnaseq](https://nf-co.re/rnaseq#introduction) (version 3.1) mainly with standard settings. Nf-core is a a community effort to collect a curated set of analysis pipelines built using Nextflow (a workflow tool to run tasks across multiple compute infrastructures in a very portable manner).

Nextflow module was already prepared by the [OIST Bioinformatic User group] (https://github.com/oist/BioinfoUgrp) making nf-core pipeline available to OIST users.
To run this pipeline we need the folowing information: samplesheet input file, reference genome file (gtt, gtf), raw fasta files. 

Sequencing data have been deposited in the NCBI Sequencing Read Archive under accession PRJNA746661

## Differential expression analysis

DESeq and enrichment analysis details: https://github.com/angelaap/NitratiruptorRNA-seq/blob/main/NitratiruptorRNA-seq.Rmd
