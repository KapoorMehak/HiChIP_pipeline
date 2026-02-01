# Pre-alignment

This prepares the reference genome for alignment.

```bash
samtools faidx GRCm38.p6.genome.fa
cut -f1,2 GRCm38.p6.genome.fa.fai > GRCm38.p6.genome
bwa index GRCm38.p6.genome.fa
