# LanguageTranslationEngToHin
constructing a language translation model in tensorflow to convert English sentences to Hindi using latest Natural Language Processing techniques like encoder-decoder architectures with gated GRU units , attention mechanisms and teacher forcing.
## Dataset 
visit https://www.clarin.eu/resource-families/parallel-corpora and download the english-hindi dataset . The dataset contain >120000 example text from various sources like ted , tides and indic2012 .
## Requirements
* Tensorflow -v >= 2.0.0
* RAM usage >= 6 GB
* Runtime ~ 2.5 hrs on tesla k80 gpu (80k training examples)
## Model Architecture
### GRU Units
   * Gated GRU units are used because they are much faster than LSTM's and perform almost the same fr considerably small to large size input sentences
   #### Architecture of GRU is as follows
![GitHub Logo](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-var-GRU.png)


