# SingleCell-rnaseq Workflow
This repository contains single cell analysis pipelines. 
## RNA Velocity
RNA velocity is a high-dimensional vector that predicts the future state of individual cells on a timescale of hours.

+ Create a conda environment with the latest  python version. Here ```3.11.5```.
  
``` conda create -n RNAvelocity ```

+ Install the following packages versions
  
``` 
pip install numpy==1.21.1 pandas==1.1.5 matplotlib==3.7.3 scanpy==1.9.6 igraph==0.9.8 scvelo==0.2.5 loompy==3.0.6 anndata==0.8.0
```
The following packages may be needed

```
pip install tqdm
pip install ipywidgets
