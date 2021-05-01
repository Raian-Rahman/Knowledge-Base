# Overview

This file contains resources for different learning materials. Also, I have compiled best resources for learning different topics here. You could also go for these resources. I would like to thank the creator of these resources for helping us out. 

# Topics

In this folder, we have added different topics covering from basic deep learning topics to advanced models and their uses. This file contains a huge number of resources. Topics on which resources are compiled are given below:

* Machine Learning Techniques
* Deep Learning Techniques
* Computer Vision Models
* Natural Language Processing Models
  * Basic Recurrent Neural Network
  * LSTM/GRU based models
  * Transformer Based Model
* Others

# Resources

## Machine Learning Techniques

- **Stanford Machine Learning Course in Coursera:**

  This is one of the best course for learning machine learning for beginners. But, one drawback of this course is the assignments are all written in matlab. So, if you don't like the course you can just run the same thing in ```python```. 

  Link: [[Machine Learning by Stanford University | Coursera](https://www.coursera.org/learn/machine-learning)]

- **StatQuest with Josh Starmer:**
  This youtube channel contains some great explanation on topics of Machine Learning. It is quite a good resource to follow. 

  Link: [StatQuest with Josh Starmer - YouTube](https://www.youtube.com/channel/UCtYLUTtgS3k1Fg4y5tAhLbw)

- **Edureka:**
  Edureka youtube channel covers a vast number of topics on machine learning techniques. Although the videos are quite lengthy but the topics are explained in a quite good manner. 

  Link: [Machine Learning Full Course - Learn Machine Learning 10 Hours | Machine Learning Tutorial | Edureka - YouTube](https://www.youtube.com/watch?v=GwIo3gDZCVQ)

  

## Deep Learning Techniques

* **Deep Learning Specialization:**

  Deep learning specialization is one of the best resources to learn the deep learning techniques. The first three courses in this specialization covers basic topics on deep learning like what is neural network and how does it work. But the later two courses are quite advanced. It covers *Convolutional Neural Network* as well as advanced model like *Transformers* which are explained in quite a handy way. 

  Link: [Deep Learning | Coursera](https://www.coursera.org/specializations/deep-learning?)

## Computer Vision

* **Object Detection: (YOLO)**
  One of the most impactful task in computer vision is object detection, which is detecting objects from a given image. There are different tutorials available to learn YOLO. The most recent version of YOLO algorithm is YOLOv5 which was implemented by Ultralytics. Their repository has a tutorial available for using their YOLOv5 implementation.

  Link: [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5)

* **R-CNN family**:
  Before YOLO, Regional CNN was used for object detection. Three different versions of R-CNN was available. Here are some blog links to learn all these in a easy way.

  Link: [Understanding Fast R-CNN and Faster R-CNN for Object Detection. | by Aakarsh Yelisetty | Towards Data Science](https://towardsdatascience.com/understanding-fast-r-cnn-and-faster-r-cnn-for-object-detection-adbb55653d97)
  Link: [R-CNN, Fast R-CNN, Faster R-CNN, YOLO — Object Detection Algorithms | by Rohith Gandhi | Towards Data Science](https://towardsdatascience.com/r-cnn-fast-r-cnn-faster-r-cnn-yolo-object-detection-algorithms-36d53571365e)

## Natural Language Processing

### Basic Recurrent Neural Network

* **Visualizing Neural Network**:
  There are different blogs and videos representing how a neural network decides the output of the hypothesis. One of the best video that i could find is the first ```5.22 min``` of a video by **Luis Serrano** 

  Link: [A friendly introduction to Recurrent Neural Networks - YouTube](https://www.youtube.com/watch?v=UNmqTiOnRfg)

* **Recurrent Neural Network Theory** 
  Recurrent Neural Network is always difficult to understand. This video explains the recurrent unit in a very simple and efficient way.

  Link: [A friendly introduction to Recurrent Neural Networks - YouTube](https://www.youtube.com/watch?v=UNmqTiOnRfg)

### Seq2Seq Models

* **Seq2Seq Model With Attention**
  In this blog the importance of seq2seq model is explained as well as how the seq2seq model works

  Link: [Visualizing A Neural Machine Translation Model (Mechanics of Seq2seq Models With Attention) – Jay Alammar – Visualizing machine learning one concept at a time. (jalammar.github.io)](https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/)

* **Seq2Seq Model generation of context**
  Encoder or Seq2Seq takes 2 input. One is the input word and the other is the context or hidden state from previous unit. What happens on each timestep can be seen from here

  Link:
  (Rolled Version): https://jalammar.github.io/images/seq2seq_5.mp4

  (Unrolled Version): https://jalammar.github.io/images/seq2seq_6.mp4

### Advanced NLP Models

* **Transformer Explained:**
  Transformer itself is the core of all nlp models nowadays. It is one of the most core things to look for. Some great resources for understanding transformer is given here:

  Link: 

  - [Illustrated Guide to Transformers Neural Network: A step by step explanation - YouTube](https://www.youtube.com/watch?v=4Bdc55j80l8)
  - [Transformers - YouTube](https://www.youtube.com/playlist?list=PLBoQnSflObckGnAS9mXjqCZhg7VTz4x8n)
  - [The Illustrated Transformer – Jay Alammar – Visualizing machine learning one concept at a time. (jalammar.github.io)](http://jalammar.github.io/illustrated-transformer/)
  - [The Narrated Transformer Language Model - YouTube](https://www.youtube.com/watch?time_continue=1&v=-QH8fRhqFHM&feature=emb_logo)

* **Transformer Code:**
  Transformer Code Walkthrough is explained in the following tutorials:
  Link:

  * [gordicaleksa/pytorch-original-transformer: My implementation of the original transformer model (Vaswani et al.). I've additionally included the playground.py file for visualizing otherwise seemingly hard concepts. Currently included IWSLT pretrained models. (github.com)](https://github.com/gordicaleksa/pytorch-original-transformer)
  * [Pytorch Transformers from Scratch (Attention is all you need) - YouTube](https://www.youtube.com/watch?v=U0s0f995w14)
  * [The Annotated Transformer (harvard.edu)](https://nlp.seas.harvard.edu/2018/04/03/attention.html)

* **Positional Encoding**:
  Positional Encoding is one of the three key contributions of original transformer paper. But there are not a lot of tutorials on positional encoding. The following blog provides a good illustration on positional encoding:

  Link: [Transformer Architecture: The Positional Encoding - Amirhossein Kazemnejad's Blog](https://kazemnejad.com/blog/transformer_architecture_positional_encoding/)

* **BERT:**
  BERT is the one of the biggest models after transformer that are being used in different Natural Language Processing tasks like text classification. One of the key changes in BERT is BERT takes the encoder of transformer and modifies it. The full form of BERT is *Bidirectional Encoder Representation of Transformer*. BERT is often used for text classification. Here are some tutorials to learn BERT:

  
  Link:

  * [The Illustrated BERT, ELMo, and co. (How NLP Cracked Transfer Learning) – Jay Alammar – Visualizing machine learning one concept at a time. (jalammar.github.io)](http://jalammar.github.io/illustrated-bert/)
  * [A Visual Guide to Using BERT for the First Time – Jay Alammar – Visualizing machine learning one concept at a time. (jalammar.github.io)](http://jalammar.github.io/a-visual-guide-to-using-bert-for-the-first-time/)
  * [BERT — transformers 4.5.0.dev0 documentation (huggingface.co)](https://huggingface.co/transformers/model_doc/bert.html#overview)
  * [notebooks/text_classification.ipynb at master · huggingface/notebooks (github.com)](https://github.com/huggingface/notebooks/blob/master/examples/text_classification.ipynb)
  * [Community — transformers 4.5.0.dev0 documentation (huggingface.co)](https://huggingface.co/transformers/master/community.html#community-notebooks)

## Others









