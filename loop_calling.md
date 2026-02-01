# Loop calling with FitHiChIP

## Convert to HiC-Pro format
```bash
grep -v '#' mapped.pairs | \
awk '{print $1"\t"$2"\t"$3"\t"$6"\t"$4"\t"$5"\t"$7}' | \
gzip -c > hicpro_mapped.pairs.gz

#FitHiChIP
bash FitHiChIP_HiCPro.sh -C fithichip_config.txt
