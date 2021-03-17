# Autoencoder for ATLAS

An autoencoder neural network was used to compress the four-momentum of jets (obtained from a sample of simulated particles) from 4 to 3 variables. This task was performed as an evaluation exercise for Google Summer of Code 2021.

### Prerequisites
The dataset and the base code were provided by the maintainers of [the ATLAS project](https://hepsoftwarefoundation.org/gsoc/projects/2020/project_ATLAS.html) at CERN.

### Concept
The dataset had to be 'cleaned' as it was obtained in the form of a ROOT data file. Data relating to only jet objects was extracted. This data was then normalised to bring the range of values of variables closer to each other.

An autoencoder LeakyReLU neural network was modelled, trained and tested on the given dataset, based on the code supplied by [the maintainers](https://hepsoftwarefoundation.org/gsoc/projects/2020/project_ATLAS.html). The neural network employed 2 layers for compression (-200-20-) and decompression (-20-200-). The activation function used was tanh(), the epoch was set to 100 and the learning rate used was one that resulted in minimal loss (as calculated using fastai learner's lr_find() module). 

### Results
The autoencoder compression neural network resulted in successful compression and reconstruction of compressed data with a MSE loss of 3.765139990719035e-05.

<b>All operations were performed in [a single jupyter notebook](https://github.com/nrishabh/atlas-autoencoder/blob/master/ATLAS%20Evaluation%20Task.ipynb). Detailed description and output of all operations can be found in the jupyter notebook itself.</b>

A simple presentation was made based on the task, which can be viewed [here](https://docs.google.com/presentation/d/1WR0Vilcxm-NACnQCgLH4SHFNKxhz0Lc99LYqbqLP_iI/edit?usp=sharing).
