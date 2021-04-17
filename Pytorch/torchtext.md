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

But, it is not a good practice to use this tokenization technique because it often fails to provide a very good output. A better way is to use spacy tokenizer. It is demonstrated below:
``` python
import spacy
!python -m spacy download en
spacy_en = spacy.load('en')

def tokenize(text):
    return [tok.text for tok in spacy_en.tokenizer(text)]
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
"""
here we specify how the data should be preprocessed
"""
#here quote is a sequential data
quote = Field(sequential = True, use_vocab = True, tokenize = tokenize, lower = True)

#score is nor a sequential data
score = Field(sequential = False, use_vocab = False)

#now we contruct a field that will be a dictionary
#it spacify which columns to use in the dataset
fields = {
    'quote' : ('q', quote), #defines how this column is going to be preprocessed using quote field
    'score': ('s', score)   #defines how this column is going to be preprocessed using quote field
}

#to access score, we could use
batch.s
```

## Load Dataset
For dataset we use TabularDataset. A demonstration is given below:
``` python
train_data, test_data = TabularDataset.splits(
                                    path = 'path_to_file',
                                    train = 'train.json',
                                    test = 'test.json',
                                    # for validation add, validation = 'validation.json'
                                    format = 'json',
                                    fileds = fields
                                )

print(train_data[0].___dict___.keys())      #to get the keys
print(train_data[0].___dict___.values())    #to get the values
```

## Build a vocabulary

``` python
quote.build_vocab(
      train_data, max_size = 10000, 
      min_freq=1, 
      vectors = 'glove.6B.100d' #1 gb download
)
```


## Construct the iterator
``` python
"""
it will do the padding for us
"""
train_iterator, test_iterator = BucketIterator.splits(
    (train_data,test_data),
    batch_size = 2,
    device = "cuda"
)
```














