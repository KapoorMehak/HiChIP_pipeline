# Library quality control

## QC statistics
```bash
python3 ./HiChIP/get_qc.py -p stats.txt

#ChiP enrichment 
./HiChIP/enrichment_stats.sh \
-g GRCm38.p6.genome \
-b mapped.PT.bam \
-p consensusChIP_peaks.bed \
-t 16 -x ChIP

#Plotting
cut -f1,2,3 consensusChIP_peaks.bed > output.bed

python3 ./HiChIP/plot_chip_enrichment.py \
-bam mapped.PT.bam \
-peaks output.bed \
-output enrichment.png
