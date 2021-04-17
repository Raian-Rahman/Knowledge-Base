# Overview
We often need to use custom data for NLP training. The most common NLP tasks are:
* Train test split: creating the train/test/validation split
* File Loading: 
* Tokenization: break the sentence into list of words
* Vocabularize: generate a vocabulary list
* Numericalize: map words into integer number together
* Word vector: generate the word embedding
* Batching: generating batches of training smaple (padding is normally happenning here)
* Embedding Lookup: map each sentence into a fixed dimension word vector

An example is given below for each task:

-> If the given text is ```The quick fox jumped over the lazy dog```. Then after tokenization, we get ```[The, quick, fox, jumped, over, the, lazy, dog]```. After vocabularize we will have:
``` python
{
    "the": 0,
    "quick": 0,
    "brown": 0,
    ...
}
```
Then after numericalizing the text we have ```[0,1,2,..]``` and during embedding lookup we have the word vectors using *GlOVE* or *Spacy Word Embedding*. 

In simple, our task is to:
1. Spacify how preprocessing should be done using ```Field```
2. Use Dataset to load the data using ```TabularDataset```
3. Construct an iterator to do batching and padding ```BucketIterator```


## Import
``` python
"""
here the legacy version is used because in 0.8.x the Field and other files were shifted to legacy version
"""
from torchtext.legacy.data import Field, TabularDataset, BucketIterator 
```

## Tokenize 
For tokenization a very simple way is to use ```split()``` function. But it is not an idea way to do these. However an easy way is shown here
``` python
tokenize = lambda x: x.split()
```

## Creating fields
To create a field, we have several parameters. 
some important parameters are:
| Parameter  	| Description                            	|
|------------	|----------------------------------------	|
| sequential 	| Set True if the data is sequential     	|
| use_vocab  	| set True if you want to use vocabulary 	|
| tokenize   	| use the tokenizer we created before    	|
| lower      	| to make the filed lowercase           |

An example is given below:
``` python

```












