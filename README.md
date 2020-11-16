# Machine Translation Model based on Encoder + Dcoder + Attention

## 1. Introduction
There are 2 models based on encoder-decoder structure. And they are uesd for French-English translation tasks.

The first model is the "encoder + simple decoder" structure, while the second model added the attention mechanism, and used two generation methods: greedy and beam search.

In the training phase, a gradually weakening teacher-forcing method is used to make the model converge as soon as possible but reduce the effect of exposure bias.

In order not to consider the weight of the padding 0 part, the necessary section of weights is intercepted before calculating the attention.

## 2. Result-Compare
### 2.1 With or without Attention
<p float="center">
  <img src="./IMG/Model%20%20without%20attention.png" width="400" />
  <img src="./IMG/Model%20%20with%20attention.png" width="400" /> 
</p>
 Model without Attention   Model with Attention 
 
### 2.2 Greedy Search or Beam Search
<p float="center">
  <img src="https://github.com/Make0930/Machine-Translation-Model/blob/main/IMG/Greedy-Search.png" width="400" />
  <img src="https://github.com/Make0930/Machine-Translation-Model/blob/main/IMG/Beam_Search.png" width="400" /> 
</p>
Greedy Search     Beam Search

## 3. Colcusion
1. For long sequences, the attention mechanism can significantly improve model performance

2. Beam search can increase the diversity of results

3. Teacher-forcing can effectively solve the problem of slow convergence and instability
