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
   * Gated GRU units are used because they are much faster than LSTM's and perform almost the same fr considerably small to large size input sentences.
   * To get a deeper understanding refer to https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21
   #### Architecture of GRU is as follows
![GitHub Logo](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-var-GRU.png)
### Encoder-Decoder Architecture
   * Encoder consists of a searies reccurent cell like traditionla RNN , GRU or LSTM . The endoder encoder the given sentence into a fixed size context vector .
   * The decoder then using the context vector decodes the sentences into target sentence using methods of conditional propabilities to minimize the loss.
   * Check out https://towardsdatascience.com/understanding-encoder-decoder-sequence-to-sequence-model-679e04af4346 for deeper insights
   
   ![GitHub Logo](https://blog.dataiku.com/hubfs/encoder%20decoder%20NLP%20architecture.png)
 
 ### Attention Mechanisms
   * While decoding certain parts of the sentences it makes more sense to look at only certain areas of the input senteces.
   ![GitHub Logo](https://3qeqpr26caki16dnhd19sv6by6v-wpengine.netdna-ssl.com/wp-content/uploads/2017/10/Depiction-of-Global-Attention-in-an-Encoder-Decoder-Recurrent-Neural-Network.png)
   * We would use Bahdanu's attention layer in this notebook . refer https://arxiv.org/pdf/1409.0473.pdf for details of the layer.
     ![GitHub Logo] (https://i.stack.imgur.com/yqJpG.png)
     


