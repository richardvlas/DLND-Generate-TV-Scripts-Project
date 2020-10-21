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
|Fully connected|output = vocab_size, activation: linear|

## Results
The trained network is used to generate a new, "fake" Seinfeld TV script of specified length `gen_length=400` and `prime_word='jerry'` to start with as shown in the snapshot example of generated script below


>jerry:, you know, you know the same thing i was going to get out of your mind.
>
>jerry: i think we can do this!
>
>jerry: i don't know. i mean, i think you should do it.
>
>elaine:(to jerry) hey, i can't get the hell outta here.
>
>george:(pointing at the phone) yeah, well, i guess i can get out of this thing.
>
>elaine: what is this?
>
>george: oh no. no, no, no. no, no.
>
>kramer: hey, hey, hey, hey, you got a little taste?
>
>jerry: i don't know.
>
>elaine: oh, no.
>
>kramer: well, i'm not going to be able to be here.
>
>george: what about?
>
>jerry: well, you know, you don't have to get to work. you don't think i was going to do it?
>
>elaine: yeah...
>
>kramer: well, you know, it's like you don't have to be interested in a while, and you know, i think i could have seen it in my apartment.
