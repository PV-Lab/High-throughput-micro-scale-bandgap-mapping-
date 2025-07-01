# High-throughput-micro-scale-bandgap-mapping

This repo contains the data and algorithms for manuscript "High-throughput micro-scale bandgap mapping for perovskite-inspired materials with complex composition space".

## Raw data
All hyperspectral imaging hypercubes, spatially-resolved spectra and bandgap analysis results can be found at https://osf.io/nx2ae/. 

## Bandgap Extraction Code
The bandgap extraction algorithm in this manuscript was adapted from **Siemenn, A. E. et al. Using scalable computer vision to automate high-throughput semiconductor characterization. Nat. Commun. 15, 4654 (2024)**. The original code is available at https://github.com/PV-Lab/Autocharacterization-Bandgap. The main changes made for better fitting and  generalizability are summirized in the table below: 
|           |    This work    |	Previous work   |
| ------    | -------------   | ------------- |
| Range     | Full data range | Manual selection of target bandgap range|
| Resolution|Spatially-resolved bandgaps (N x N spectra)  |Average bandgap of each droplet (1 spectrum) |
|  Fitting	|Linear regression on maximum difference | Linear regression on detected peaks |
