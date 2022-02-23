# RNA-Seq Analysis of Capsicum annuum-Xanthomonas pathosystem under Elevated O3
## Introduction
This repository contains a bioinformatic pipeline that takes in raw fq files, and will output graphics displaying differentially expressed genes in Xanthomonas tolerant an susceptible lines of pepper. 

## Objective
Tropospheric ozone is one of many greenhouse gases that is an increasingly dangerous pollutant to natural ecosystems around the world. Levels will continue to increase with current greenhouse gas emissions and future climate models, with predictions showing an 8% increase in O3 by 2100. O3 remains one of the most harmful air pollutants to crops, causing early senescence, scoring of leaves, and reduced gas exchange. An aspect of crop life that has not received enough coverage yet includes how elevated O3 conditions will impact plant defenses to pathogens.

I aim to examine the Capsicum annuum-Xanthomonas pathosystem, and how this pathosystem will be effected in the presence of elevated tropospheric ozone. This pathosystem is viable to study given the effectiveness of Xanthomonas bacterial spotting is on Solonaceaous species, especially in our region in the southeastern United States. In using the following bioinformatic pipeline, I hope to provide a detailed process on how we were able to sequence RNA transcripts to understand the regulation and crosstalk of common pathogen and O3 defense genes in Capsicum annuum. 

contribute to these phenotypes in model organisms are genetically divergent/differentiated in these garter snake ecotypes. To this aim, we will calculate Tajima's D, Fst, and Dxy in pair-wise fashion to understand whether inter-ecotypic (within) population comparisons significantly differ from intra-ecotypic (between) population comparisons.

![Projected-Pipeline](./Bioinfographic.png)
Pipeline follows close to this Nature [protocol](https://doi.org/10.1038/nprot.2016.095)
## Dependencies
Recommended to be used on a high performance cluster/ supercomputer with a job submission system. Alabama Super Computer used for original procedure. 
## Scripts
1. Bash script to process genomic data ([fastqc](https://github.com/s-andrews/FastQC), [gatk](https://gatk.broadinstitute.org/hc/en-us)) and filter sequence variants ([bcftools](https://samtools.github.io/bcftools/bcftools.html)).
2. Python script to trim Illumina adapters used during sequencing using [cutadapt](https://cutadapt.readthedocs.io/en/stable/).
3. Bash script to use [HISAT2](http://daehwankimlab.github.io/hisat2/), and [stringtie](https://ccb.jhu.edu/software/stringtie/) for read alignment, assembly and expression estimation. 
4. R script to provide statistics on differentially expressed transcripts and graphics to display results of the analysis. Statistics done using [ballgown](https://www.bioconductor.org/packages/devel/bioc/manuals/ballgown/man/ballgown.pdf)
