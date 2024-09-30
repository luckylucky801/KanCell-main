[![Documentation Status](https://readthedocs.org/projects/kancell/badge/?version=latest)](https://kancell.readthedocs.io/en/latest/?badge=latest)
![PyPI](https://img.shields.io/pypi/v/KanCell)

# KanCell: Augmented Dissection of Cellular Heterogeneity in Biological Tissues through Integrated Single-Cell and Spatial Transcriptomics

![](docs/_static/img/figure1.png "Overview")


## Getting started
* [Requirements](#Requirements)
* [Installation](#Installation)
* Tutorials
    * [Deconvolution of cell types composition on breast cancer dataset](docs/tutorials/breast cancer.ipynb)
    * [Deconvolution of cell types composition on human_heart dataset](docs/tutorials/human_heart.ipynb)
    * [Deconvolution of cell types composition on melanoma dataset](docs/tutorials/melanoma.ipynb)
    * [Deconvolution of cell types composition on STARmap dataset](docs/tutorials/STARmap.ipynb)




## Latest updates
### Version 1.1.6 2023-07-27
#### Fixed Bugs
- Fixed a bug regarding the similarity loss weight hyperparameter `simi_l`, which in the previous version did not affect the loss value.

### Version 1.1.5 2023-07-26
#### Fixed Bugs
- Fixed a bug in the similarity loss of Splane, where it minimized the cosine similarity of the latent vectors of spots with their neighbors.
#### Features
- Optimized the time and memory consumption of the Splane training process for large datasets.

### Version 1.1.2 2023-07-12
#### Fixed Bugs
- Removed `rpy2` from the pypi dependency of KanCell. It now needs to be pre-installed when creating the environment through conda.
- Fixed a bug in Scube where the `best_model_state` was not referenced before being used.
#### Features
- Added function documentations for Scube related to the GPR model.
    
## Requirements
**Note**: The current version of KanCell only supports Linux and MacOS, not Windows platform. 

To install `KanCell`, you need to install [PyTorch](https://pytorch.org) with GPU support first. If you don't need GPU acceleration, you can just skip the installation for `cudnn` and `cudatoolkit`.
* Create conda environment for `KanCell`:
