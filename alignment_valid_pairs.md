# Alignment and valid pair generation

## Alignment
```bash
bwa mem -5SP -T0 -t16 GRCm38.p6.genome.fa \
HiChIP_R1.fastq.gz HiChIP_R2.fastq.gz > aligned.sam

#Pair parsing and filtering
pairtools parse --min-mapq 40 \
--walks-policy 5unique \
--max-inter-align-gap 30 \
--chroms-path GRCm38.p6.genome \
aligned.sam > parsed.pairsam

#Sorting and deduplication
pairtools sort --nproc 16 parsed.pairsam > sorted.pairsam
pairtools dedup --mark-dups --output-stats stats.txt \
--output dedup.pairsam sorted.pairsam

#BAM generation
pairtools split --output-pairs mapped.pairs \
--output-sam unsorted.bam dedup.pairsam

samtools sort -@16 -o mapped.PT.bam unsorted.bam
samtools index mapped.PT.bam
