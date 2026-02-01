# Visualization

## Juicer
- Interactive contact maps
- 1D and 2D annotations
- Normalization and resolution control

## HiGlass
```bash
docker pull higlass/higlass-docker:v0.6.1
docker run --publish 8989:80 --volume ~/hg-data:/data higlass/higlass-docker
