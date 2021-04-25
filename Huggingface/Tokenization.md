# Overview
For any machine learning task, we need map the raw input into a representation that is understnadable by a tranable model. It is more important in the case of sequence models, more specifically text input. 

In case of text input we could simply use split to split the word and make a map to tokenize each and every words. In code the task is very simple:
``` python
s = "something very long ..."
words = s.split(" ")
vocabulary = dict(enumurate(set(words))) #maps a string's word by its corresponding ID
```

This approach might work well if your vocabulary remains small as it would store every word (or token) present in your original input. Moreover, word variations like "cat" and "cats" would not share the same identifiers even if their meaning is quite close.

## Subtoken Tokenization
To overcome the issues described above, recent works have been done on tokenization, leveraging "subtoken" tokenization. Subtokens extends the previous splitting strategy to furthermore explode a word into grammatically logicial sub-components learned from the data.

Taking our previous example of the words cat and cats, a sub-tokenization of the word cats would be [cat, ##s]. Where the prefix "##" indicates a subtoken of the initial input. Such training algorithms might extract sub-tokens such as "##ing", "##ed" over English corpus.

As you might think of, this kind of sub-tokens construction leveraging compositions of "pieces" overall reduces the size of the vocabulary you have to carry to train a Machine Learning model. On the other side, as one token might be exploded into multiple subtokens, the input of your model might increase and become an issue on model with non-linear complexity over the input sequence's length.
