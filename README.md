# ECBC
Collection of scripts for error correcting antibody sequening

## IgG Reads
- R1: fwd 4N, leader, variable
- R2: rev subtype determination, constant, variable
- I1: EVBC 12
- I2: sample

## klMA Reads
- R1: fwd 4N, leader, variable
- R2: rev ECBC 12, spacer 4, constant, variable
- I1: LC index TAAGGCGAGAGC 12
- I2: sample

## Workflow

`pipeline.sh`
- script that calls all the later ones

`IgG_klMA_ECBC.py`
- pandaseq R1 und R2split into IgG vs. klMA
- for HC get IgG subtypes
- for LC get ECBE, klMA discrimination
Usage: `IgG_klMA_ECBC.py NAME_L001_R1_001.FASTQ(.GZ)`

`CH_primer_trim.py`
- tim CH region and fwd primers
- fwd primer in leader region
- CH sequence inlcuding primers
Usage: `CH_primer_trim.py SAMPLE_panda.fasta trim_fwd_primer.fasta trim_CH.fasta`

`indices`
- count indices (only indices present >10 ?)
- collapse indices —> consensus (check for variation)


## Primers


## Chunks

`pandaseq.py`