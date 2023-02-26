escribi por mi cuenta el README.md del sitio : [Machine-Learning-Tokyo /
Poetry-GAN
Public](https://github.com/Machine-Learning-Tokyo/Poetry-GAN/blob/master/README.md)
:bar_chart:

# **Creative GAns**

Creative GANs is a research project on training language models to generate creative text with either a Maximum Likelihood Estimation (MLE) or GAN objective. It contains the code for running the experiments as described in the [paper](https://arxiv.org/abs/1909.09534).

Some curated outputs can be found [here](https://www.ai-fragments.com/)

## Datasets

- Gutenberg Novels
- English poety
- Song lyrics
- [Metaphors](http://metaphors.iath.virginia.edu/metaphors)

## Text Generative Models with LM and Gan objective

- AWD LSTM [paper link](https://arxiv.org/pdf/1708.02182.pdf)
- Transformer XL [paper link](https://arxiv.org/pdf/1901.02860.pdf)

The encoder models are from the fastai library

## Usage

- Preprocess data `python preprocess.py [gutenberg/metaphors/poems/lyrics]`
- Train language model `lang_model.py PATH FILENAME MODEL [PRETRAINED_FNAMES]`
- Train gan model `textgan.py PATH FILENAME PRETRAINED MODEL [CRIT] [PREDS] [EPOCHS]`

```
PATH - folder with data
FILENAME - name of preprocessed file
PRETRAINED - fastai model saved with learn.save()
PRETRAINED_FNAMES - pretrained weight file and vocab file (comma seperated)
MODEL - architecture to use {'AWD': AWD_LSTM, 'XL':TransformerXL}
CRIT - loss function: gumbel softmax/reinforce (only for gan)
PREDS - generate output from validation set
EPOCHS - number of epochs to train

```
