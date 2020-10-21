# Generate TV Scripts 

## Project Overview
In this project, I've build a recurrent neural network from scratch to generate new Seinfeld TV scripts using RNNs. As training data a Seinfeld dataset of scripts from 9 seasons is used. The Neural Network that I built generates a new, "fake" TV script.

### Project Files
The project includes the following files:
* `README.md` - A markdown file explaining the project structure and training approach and new generated "fake" TV script
* `dlnd_tv_script_generation.ipynb` - Jupyter Notebook describing the project
* `dlnd_tv_script_generation.html` - HTML version of the Jupyter Notebook
* `helper.py` - python code for loading and preprocessing data
* `problem_unittests.py` - unit tests for each part of the project code

## Neural Network Model Architecture
The neural network is build in PyTorch and implements an RNN architecture with Long Short-Term Memory (LSTM) cells using PyTorch's [Module class](http://pytorch.org/docs/master/nn.html#torch.nn.Module). The following table shows the final model architecture


|Layer|Description|
|---|---|
|Embedding|embedding dims = 400|
|LSTM|#layers = 2, hidden dims = 256, drop_prob = 0.5|
|Dropout|drop_prob = 0.3|
|Fully connected|output = vocab_size, activation: linear|
