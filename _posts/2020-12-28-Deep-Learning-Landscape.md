---
toc: true
layout: post
description: Going on a deep learning adventure
categories: [post]
title: Deep Learning Landscape 
---

Here we try to understand Deep Learning landscape....

​ credits : [forbes
images](https://thumbor.forbes.com/thumbor/960x0/https%3A%2F%2Fblogs-images.forbes.com%2Fbernardmarr%2Ffiles%2F2018%2F10%2FAdobeStock_179912599-1-1200x797.jpg)

Written by: [Aryan Nath](https://www.linkedin.com/in/aryan-nath-7324aa200/)

Reviewed by: [Ankit Rathi](https://www.linkedin.com/in/ankitrathi/)

Well most of us are already familiar with the idea of what **deep learning** is
if not, then let’s quickly remind our self what it is.

**Deep learning** is a sub field of a much broader filed called machine learning
, basically when our computer does something for us which is similar to
something which only a human brain can do is called **deep learning** .

Deep learning models can do complex tasks from **image classification** to
**completing sentences** for us, and with the recent development in the field
the it has gone to producing **deep fakes** (of anyone) [some more breakthroughs
in
2019.](https://analyticsindiamag.com/top-7-artificial-intelligence-breakthroughs-we-saw-in-2019/)

As we mentioned earlier that *deep learning* was a subset of machine learning ,
so what exactly is machine learning let’s see

![](https://cdn-images-1.medium.com/max/800/0*r9fVFdCbW77-p8NG){:width="100%"}

​ credits: [geo spaitial
media](https://geospatialmedia.s3.amazonaws.com/wp-content/uploads/2017/05/AAEAAQAAAAAAAAhPAAAAJDlkMWMwNTA1LTZkZjUtNDA5MS1hYT.jpg)

* **MACHINE LEARNING** :- “ *Machine Learning is the study of computer algorithms
that improve automatically through experience* “ , by [Tom
Mitchell](http://www.cs.cmu.edu/~tom), McGraw Hill, 1997. it is the development
of computer systems which will which will learn and adapt to new situations
without explicitly giving it instructions for everything.
* **DEEP LEARNING** :- It is where specifically designed algorithms are used to
mimic the human brain in solving real world problems. Where the algorithms will
learn from data provided by us in order to get to the desired results.
* **ARTIFICIAL INTELLIGENCE** :- It is the parent term for both *deep and machine
learning* , it is intelligence shown by any machine , which is in some way
exactly or more accurate than human brain.

### WHEN TO USE DEEP LEARNING

### <br> 

So now the question is when should we use deep learning for our tasks and how
will we implement it ? and is it the answer for all our questions ? Is it really
capable of doing everything or it too have some limitations?

![](https://cdn-images-1.medium.com/max/800/0*16Og_qtitvIemOn4){:width="100%"}

​ credits: [the news
stack](https://cdn.thenewstack.io/media/2020/05/6a5f470b-02.png)

Machine learning has been around for long that is how google always knew how to
sort the web pages and how to only show the most relevant pages on top.
**Traditional machine learning ** still with many advancements it require a lot
of human intervention and a lot more work needs to be done in making the normal
machine learning algorithm to adapt to even similar looking tasks.

![](https://cdn-images-1.medium.com/max/800/0*YUyMSFUKc2C-LcQ7){:width="100%"}

​ credits:
[abyssal](https://abyssal.eu/wp-content/uploads/AbyssalAi-traditional_vs_deep-performance.png)

This is where *deep learning* slides in it requires least human interactions and
most of the deep learning algorithms are good at adapting like a human brain.
**Complex problems** and **data** also plays an important part in this , where
old machine learning is not equipped to handle complex problems like recognizing
faces which requires a huge dataset (sometimes of millions of data points) ,
deep learning algorithms can handle it quite smoothly. But with larger data we
also need **more computation power** which is expensive in nature .

**An example-** When we will classify dogs and cats using deep learning
technique like neural nets there is no need for a programmer to intervene to
write code or select the variable required to make the difference , our model
will automatically do that for us , but we will require a dataset to train our
model on.

Deep learning cannot be used for every problem it is not the ultimate answer to
everything. Some common drawbacks are:-

* It is not always easy to get the data we require which we will feed our model.
* Data should be diverse otherwise it may lead to biased predictions.
* Not every machine learning practitioner will be equipped to pay for **high end
GPU’s**
* Deep learning can become exceptionally well in specific domains but for now it
is still far from attaining human like intelligence.

### How deep learning works

![](https://victorzhou.com/media/nn-series/network.svg){:width="100%"}

​ credits: [victorzhou](https://victorzhou.com/media/nn-series/network.svg)

Deep learning models are made up of many layers of nodes , which is called a
**neural network** . Just like a human brain has neurons to transmit the data
here we have nodes which work similar to as that of neurons.

A neural network is a series of algorithm which work to find relationships
between the data provided and to find useful patterns just like a human brain.
In an **artificial neural network** the interconnected layers of neurons perform
mathematical calculations ,for finding meaningful information and relations in
our data. They are used as decision making tools which can model complex
relation between input and output and mold its structure based on those
relations. Artificial neurons were first proposed in 1943 by [Warren
McCulloch](https://en.wikipedia.org/wiki/Warren_Sturgis_McCulloch), a
neurophysiologist, and [Walter
Pitts](https://en.wikipedia.org/wiki/Walter_Pitts), a logician, who first
collaborated at the [University of
Chicago](https://en.wikipedia.org/wiki/University_of_Chicago).

In a neural network each node to the next node has a link which is a
mathematical function ,where each link has a weight which determines it’s
influence on the next node. It’s done by first getting the weighted sum of the
inputs and then adding bias to it so that we may get the activation of the next
node. These activations are used to then determine the outputs of our neural
network.

### DIFFERENT DEEP LEARNING NETWORKS

### <br> 

#### Convolution Neural Networks (CNN) :-

![](https://cdn-images-1.medium.com/max/800/0*fmQL3BX7PLybKTww){:width="100%"}

#### <br> 

#### <br> 

​ credits: [analytics
vidhya](https://cdn.analyticsvidhya.com/wp-content/uploads/2020/02/1oB3S5yHHhvougJkPXuc8og.gif)

These types of neural nets are mostly used in image and video processing , CNN
learns automatically without giving specific commands ,these feature of good
data extraction from input data makes it suitable for image processing models.
These type of neural networks use convolution in place of general matrix
multiplication in at least one of their layers.

### Recurrent Neural Network (RNN) :-

### <br> 

![](https://cdn-images-1.medium.com/max/800/0*4cXXePDytdlgX57H){:width="100%"}

​ credits: [medium](https://miro.medium.com/max/1039/0/8AfmjQTGGEmEFxIa.png)

In RRN’s the output from the previous step is taken as inputs for the current
step. Here neurons in the hidden layer receive input with a certain delay in
time , so this neural net is used where there are certain iteration in
information. It is prevalent in most of the time series analysis because it can
remember previous inputs also, and also text completion models.

![](https://cdn-images-1.medium.com/max/800/0*aNpWclaw16LIabsK){:width="100%"}

​ credits: [medium](https://miro.medium.com/max/785/030h4uFH8GxOT23fk.png)

An autoencoder is a type of neural net where the network learns in an
unsupervised manner .These type of neural nets try to copy the input to the
output , where they have the input cells greater than the hidden cells and
usually the input cells is equal to the output cells. It is mainly used in
classification and feature compression problems.

### Generative Adversarial Network (GAN):-

### <br> 

![](https://cdn-images-1.medium.com/max/800/0*OMAARZtRmalNcjiY){:width="100%"}

​ credits: [medium](https://miro.medium.com/max/1091/0/wDTai055oQ7F0AoW.png)

GAN’s are used to create new data using the data on which our model is trained.
It is one of the most interesting aspects of deep learning that something new
can be created . Example — if we train our network on a dataset of something
specific it can somehow create something that looks similar to the ones we
trained our model on.

#### References :

* [https://medium.com/towards-artificial-intelligence/main-types-of-neural-networks-and-its-applications-tutorial-734480d7ec8e](https://medium.com/towards-artificial-intelligence/main-types-of-neural-networks-and-its-applications-tutorial-734480d7ec8e)
* [https://www.analyticsvidhya.com/blog/2020/02/cnn-vs-rnn-vs-mlp-analyzing-3-types-of-neural-networks-in-deep-learning](https://www.analyticsvidhya.com/blog/2020/02/cnn-vs-rnn-vs-mlp-analyzing-3-types-of-neural-networks-in-deep-learning)
* [https://www.simplilearn.com/tutorials/deep-learning-tutorial/what-is-deep-learning](https://www.simplilearn.com/tutorials/deep-learning-tutorial/what-is-deep-learning)
* [https://towardsdatascience.com/why-deep-learning-is-needed-over-traditional-machine-learning-1b6a99177063](https://towardsdatascience.com/why-deep-learning-is-needed-over-traditional-machine-learning-1b6a99177063)
* [https://en.wikipedia.org/wiki/Artificial_intelligence](https://en.wikipedia.org/wiki/Artificial_intelligence)

