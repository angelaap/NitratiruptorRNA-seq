# NitratiruptorRNA-seq
This repository includes the generated code for Nitratiruptor transcriptome analysis under metal stress (i.e. Cd, Cu) and intermediate files created. 

## From raw fasta files to transcript counts

FASTA files were processed using the Nextflow [nfcore/rnaseq](https://nf-co.re/rnaseq#introduction) (version 3.1) mainly with standard settings. Nf-core is a a community effort to collect a curated set of analysis pipelines built using Nextflow (a workflow tool to run tasks across multiple compute infrastructures in a very portable manner).

Nextflow module was already prepared by the [OIST Bioinformatic User group](https://github.com/oist/BioinfoUgrp) making nf-core pipeline available to OIST users.
To run this pipeline we need the folowing information: 

* samplesheet input file 
* [reference genome file (gtt, gtf)](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/000/010/325/GCA_000010325.1_ASM1032v1/)
* raw fasta files: sequencing data have been deposited in the NCBI Sequencing Read Archive under accession PRJNA746661

Nextflow pipeline nfcore/rnaseq (version 3.1) was used mainly with standard settings. However, the few changes made to the settings are summarized as follows: 
* strandedness of the library was set as reverse in the input file 
* Hisat2 was the aligner selected
* Trim Galore clipped length was changed to 15 bp. 



Reads were mapped to the reference sequence Nitratiruptor sp. SB155-2 (GenBank: Assembly: GCA_000010325.1). Gene counts for each sample were extracted from StringTie results using the python script, [prepDE.py](https://linuxtut.com/en/27db85f39f3ae385f451/) and imported into the R statistical environment for further analysis.


## Differential expression analysis

DESeq and enrichment analysis details: https://github.com/angelaap/NitratiruptorRNA-seq/blob/main/NitratiruptorRNA-seq.Rmd
