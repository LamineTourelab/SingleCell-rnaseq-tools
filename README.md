# SingleCell-rnaseq Workflow
This repository contains single cell analysis pipelines. 

## RNA Velocity 

RNA velocity is a high-dimensional vector that predicts the future state of individual cells on a timescale of hours.

### With scVelo

scVelo can be used to analysis RNA velocity, latent time, driver identification. See [scVelo](https://scvelo.readthedocs.io/en/stable/).

First of all, the input data for scVelo are two count matrices of pre-mature (unspliced) and mature (spliced) abundances, which can be obtained from standard sequencing protocols, using the velocyto or kallisto counting pipeline. Here is velocyto example:

```
velocyto run10x -m repeat_msk.gtf mypath/sample01 somepath/refdata-cellranger-mm10-1.2.0/genes/genes.gtf
```
Where genes.gtf is the genome annotation file provided with the cellranger pipeline. repeat_msk.gtf is the repeat masker file. See [Velocyto.org](https://velocyto.org/velocyto.py/index.html).


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
```
### Cellrank using rna velocity

Using the same conda environment ```RNAvelocity```

Install cellrank with conda:

```conda install -c conda-forge cellrank```

## Expimap

ExpiMap learns to map cells into biologically understandable components representing known ‘gene programs’. The activity of each cell for a gene program is learned while simultaneously refining them and learning de novo programs.

```
git clone https://github.com/theislab/scarches
cd scarches
conda env create -f envs/scarches_linux.yaml
conda activate scarches
```
