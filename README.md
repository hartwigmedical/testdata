# testdata

This repository contains test data for various bioinformatic tools/pipelines.

## cancerPanel test data

The following steps were taken to generate the data:
  * create BED file with regions
  * sambamba view to select reads in those regions
  * picard tools SamToFastq to create R1 + R2 fastq
  * bwa mem to map them back to reference genome
  * sambamba sort, index and flagstat in inspect

The data originates from a GIAB triple, so is biologically not representative!

Update 200714: added some COLO829 reads to CPCT12345678R and CPCT12345678T from two genomic regions that contain a variant which passes SAGE somatic caller. These reads are taken from flowcell AHHKYHDSXX dataset (where S12=COLO829T and S13=COLO829R).

## 100k_reads_hiseq

This data are just 100k (random) reads from 3 samples. Can be used for technical testing but most algo's wont be able to do anything meaningful since coverage is extremely low. 
