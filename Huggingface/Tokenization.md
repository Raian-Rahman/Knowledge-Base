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

