# portuguese-clinical-pos-tagger
A portuguese clinical POS-Tagger model trained with Flair.

The scripts included in this repository were developed in the paper [**Defining a state-of-the-art POS-tagging environment for Brazilian Portuguese clinical texts**](https://link.springer.com/article/10.1007/s42600-020-00067-7).

You are free to use the available model, as long as you cite properly.

You can download the model here [**PUCPR-FLAIR-CLINICAL-POS-TAGGING-MODEL**](https://drive.google.com/file/d/1EfoO_DzW5-TGvphp3tUMZlEAcYgFPD8J/view?usp=sharing), or load it directly from your code.

```python
from flair.data import Sentence
from flair.models import SequenceTagger

# Load our portuguese clinical model
tagger = SequenceTagger.load('pt-pos-clinical')

# Create a sentence
sentence = Sentence("Quadro de dor torácica compatível com angina instável de alto risco")
    
# Predict the POS-tags
tagger.predict(sentence)

# Print tagged sentence
print(sentence.to_tagged_string())
```

A complete tutorial on how to load the model into Flair and use the POS-Tagging can be found here: [Flair Tagging Tutorial](https://github.com/flairNLP/flair/blob/master/resources/docs/TUTORIAL_2_TAGGING.md)
