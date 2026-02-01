# Alignment and valid pair generation

## Alignment
```bash
bwa mem -5SP -T0 -t16 GRCm38.p6.genome.fa \
HiChIP_R1.fastq.gz HiChIP_R2.fastq.gz > aligned.sam
