# Contact matrix generation

## Juicer (.hic)
```bash
java -Xmx48g -jar juicer_tools.jar pre \
--threads 16 mapped.pairs contact_map.hic GRCm38.p6.genome

#cooler
bgzip mapped.pairs
pairix mapped.pairs.gz

cooler cload pairix -p 16 \
GRCm38.p6.genome:1000 mapped.pairs.gz matrix_1kb.cool

cooler zoomify --balance -p 16 matrix_1kb.cool > matrix_1kb.mcool
