
Note: This twitter chatbot is based on modifications to tensorlayer repository seq2seq chatbot https://github.com/tensorlayer/seq2seq-chatbot/ with License listed here https://github.com/tensorlayer/tensorlayer/blob/master/LICENSE.rst. Some things will oscillate between modified and original form as I keep testing what I can/cant break. Twitter chatbot, so offensive/rude output not uncommon. 

Seq2Seq file isn't well documented license-wise, so not sure if text scrapers and other non-tensorlayer code are from tensayler people or not. Of course there are plenty of of other seq2seq chatbots using the Cornell database (which is famous for that application now) plenty that use twitter and some with mostly same readme as well. I'll just clarifiy that I don't own it, I'm just playing with it. 

# Seq2Seq Chatbot

This is a 200 lines implementation of Twitter/Cornell-Movie Chatbot, please read the following references before you read the code:

- [Practical-Seq2Seq](http://suriyadeepan.github.io/2016-12-31-practical-seq2seq/)
- [The Unreasonable Effectiveness of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/)
- [Understanding LSTM Networks](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) (optional)

### Prerequisites

- Python 
- [TensorFlow](https://github.com/tensorflow/tensorflow) >= 1.2
- [TensorLayer](https://github.com/zsdonghao/tensorlayer) >= 1.6.3

### Model

<table class="image">
<div align="center">
    <img src="http://suriyadeepan.github.io/img/seq2seq/seq2seq2.png"/>  
    <br>  
    <em align="center"></em>  
</div>
</table>

### Training

```
python main.py --batch-size 32 --num-epochs 50 -lr 0.001
```

### Inference

```
python main.py --inference
```

### Results

```
Query > happy birthday have a nice day
 > thank you so much
 > thank babe
 > thank bro
 > thanks so much
 > thank babe i appreciate it
Query > donald trump won last nights presidential debate according to snap online polls
 > i dont know what the fuck is that
 > i think he was a racist
 > he is not a racist
 > he is a liar
 > trump needs to be president
