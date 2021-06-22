# Fed-Goodreads ✍️
Federated version of Goodreads spoiler subset dataset
[Goodreads](https://sites.google.com/eng.ucsd.edu/ucsdbookgraph) is a publicly available dataset and commonly used for text classification with DL due to its large volume.
Fed-Goodreads contains the book reviews subset with parsed spoiler tags is used (1.38m reviews) to perform a binary classification task of predicting if a review sentence contains a spoiler or not.
This dataset provides an ideal peronsalised setting for a federated dataset as the data is organised by individual users, where a user will have different quantities of data and different users have different patterns of writing sentences. 

Fed-Goodreads contains 100 unique clients; the number of samples per client is limited to 2-10 to enforce statistical heterogeneity; and each data sample contains 2517 features.

## Setup
To generate the dataset follow the ```generate``` jupyter notebook instructions.

## Usage
This dataset is compatible with the [FedProx](https://github.com/litian96/FedProx), FedSim implemenations. If you are using the same experiment setup simply add the following into the main.py,

```python
DATASETS = [....., 'goodreads']

MODEL_PARAMS = { ..... , 
    'goodreads.mclr': (2,), 
}

```

Reference models are availble in the FedSim implementation here.
