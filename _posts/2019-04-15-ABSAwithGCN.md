---
layout: post
title: "Aspect Based Sentiment Analysis with Gated Convolutional Networks"
description: "Aspect Based Sentiment Analysis with Gated Convolutional Networks"
slug: ABSA_GCN
category: paper
tags: []
---
{% include JB/setup %}
这篇论文介绍了基于方面的情感分析，提出了一种基于卷积神经网络和门控单元的神经网络，叫做GCAE（Gated Convolutional network with Aspect Embedding），没有使用RNN，大大地提高了模型训练的可并行性，使得训练速度大幅度加快，并且比之前基于RNN（GRU、LSTM等）的模型的效果要有提高，虽然提高不多，但是能在不使用RNN的情况下也算是不错了，毕竟该模型最大的优点是提高训练速度，节省训练时间。

**论文地址**：<https://www.aclweb.org/anthology/P18-1234>  
**论文笔记**：<https://zhuanlan.zhihu.com/p/50284374>  
**论文代码**：<https://github.com/wxue004cs/GCAE>  
### （1）模型创新与贡献
与一般模型不同，作者认为使用RNN和Attention机制都会使得模型的训练过程难以并行运算，这大大影响了训练速度，因此尝试仅仅使用CNN和一些门控单元就在保证模型效果的情况下，提高训练速度，毕竟CNN是可并行运算的。
最后，事实证明，作者确实提高了运动速度，并且模型准确率比之前的模型还要高一些。 
与其他模型的收敛时间对比如下如所示：  
![收敛时间对比](//images/posts/absa_with_gcn-1.png)   
### （2）模型介绍

