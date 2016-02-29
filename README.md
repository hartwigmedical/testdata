# giabBasedTestData

This repository contains test data for various bioinformatic tools/pipelines.

## Steps taken to create test data:

  * create BED file with regions
  * sambamba view to select reads in those regions
  * picard tools SamToFastq to create R1 + R2 fastq
  * bwa mem to map them back to reference genome
  * sambamba sort, index and flagstat in inspect
