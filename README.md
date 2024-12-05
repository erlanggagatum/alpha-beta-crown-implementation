
# α,β-CROWN (alpha-beta-CROWN) Implementation

This is a submission by Gatum Erlangga for Neural Network Verification class

## Setup and Installation
The setup and installation is based on alpha-beta-CROWN official documentation on [GitHub](https://github.com/Verified-Intelligence/alpha-beta-CROWN).

The code is run on ```python==3.11```, with ```conda``` as the environment and package manager.

First, download the tools from GitHub
```
git clone --recursive https://github.com/Verified-Intelligence/alpha-beta-CROWN.git

```
Setup conda environment 
```
# Remove the old environment, if necessary.
conda deactivate; conda env remove --name alpha-beta-crown
# install all dependents into the alpha-beta-crown environment
conda env create -f complete_verifier/environment.yaml --name alpha-beta-crown
# activate the environment
conda activate alpha-beta-crown
```

Update these packages to support implementation using newer library
```
pip install --upgrade torch torchvision
pip install matplotlib
pip install arguments
```

Download this repository which contains the implementation of SqueezeNet and fashion_mnist.
```
git clone https://github.com/erlanggagatum/alpha-beta-crown-implementation.git
```

Move these files and directories to alpha-beta-CROWN directory:
- ```custom_model_data.py``` to  ```complete_verifier/custom/custom_model_data.py```
- ```/fashion_mnist_squeezenet``` to ```complete_verifier/models/fashion_mnist_squeezenet```
- ```custom_fashion_mnist_data_squeezednet_model.yaml``` to ```complete_verifier/exp_configs/tutorial_examples/custom_fashion_mnist_data_squeezednet_model.yaml```

## Run Verification
Run the following command to perform verification on SqueezeNet and fashion_mnist dataset. Make sure all files from this repository already being moved to the alpha-beta-CROWN.

``` 
python abcrown.py --config exp_configs/tutorial_examples/custom_fashion_mnist_data_squeezednet_model.yaml
```

## Author
- [@erlanggagatum](https://www.github.com/erlanggagatum)