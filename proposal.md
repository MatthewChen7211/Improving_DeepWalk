--- 
layout: page 
title: "Project Proposal"
---

## Project Title 

Improving DeepWalk: Online Learning of Social Representations

## Project URL 

[Project Home Page](http://dongyuli.github.io/parallel_deepwalk/)

## Project Description

I will be conducting research under the guidance of Professor Yiming Yang, who is professor of Language Technology Institute and Machine Learning Department at CMU, and her PhD student Yuexin Wu.

To explain the terminologies in my project title, I will start with Natural Language Processing (NLP). A fundamental problem in this area is that texts are made of words, but computers can only deal with numbers directly. So it is natural to turn words into numbers. Word2vec is a model that does exactly that. It produces word embeddings that map words to vectors of real numbers. It preserves semantic and syntactic relations between words. For example, the vector of “brother” - the vector of “man” + the vector of “woman” is very close the vector of “sister”.

There are two algorithms in word2vec, namely CBOW (continuous bag of words) and skip-gram. The difference is that CBOW uses context (surrounding words) to predict word, and skip-gram uses word to predict context. The output of these two algorithms, however, are the same. Both of them produce word embedding, or mappings from words to numerical vectors. The empirical difference in performance is that CBOW is faster to train and tends to work better on frequent words, while skip-gram tends to work better on rare words.

So what do word2vec, CBOW, and skip-gram have to do with my research? My project is based on the paper DeepWalk: Online Learning of Social Representations, which tries to learn representations of vertices in a network. Here social representations is just one of the many applications of graphical input. For example, in a social network, vertices are users and edges are their relations such as friendship. If we want to perform some analysis on the network, it is easier for many statistical methods to work on representations of the network learned from the information of the vertices and edges than to work on the original network itself. The approach adopted by the paper is to use information from random walks in the network to learn representations by treating walks as sentences and then applying NLP methods to them. Here, the NLP method they use is skip-gram. However, the algorithm is modified to fit in the context of graphs, and the differences between skip-gram and CBOW under the modifications are not well-studied.

So I plan to first implement CBOW and skip-gram to have a better understanding of word embeddings. Then I will replace skip-gram by CBOW in DeepWalk and analyze their differences. Finally I will explore other ways to improve DeepWalk or other algorithms to learn graph representations.

The biggest challenge is that I am not familiar with machine learning on graphical input, as most of my previous experience has been focusing on image or text input. Also we are modifying established models, which could potentially lead to unexpected issues from my experience, and the result, namely the differences between CBOW and skip-gram in DeepWalk, is unknown.

On the other hand, my project could have a big impact. Word2vec is a basic model used in many NLP products on the market, and a better understanding of the differences between CBOW and skip-gram is always a good thing. Also, DeepWalk may be applied to social networks and recommendation systems, both of which are changing our lives today. I find this project interesting as it is interdisciplinary in the realm of machine learning, as it applies NLP methods to graphical input. My project could be important because word2vec and DeepWalk are baselines of many ongoing researches lately.

## Project Goals

I plan to first implement CBOW and skip-gram to have a better understanding of word embeddings. Then I will replace skip-gram by CBOW in DeepWalk and analyze their differences. Finally I will explore other ways to improve DeepWalk or other algorithms to learn graph representations.

The DeepWalk paper uses a metric called Micro-F1 to evaluate the result of multiclass classification and the sensitivity to different parameters. I also plan to use this metric and compare my result to the paper’s.

A 100% goal is a detailed analysis of the differences between CBOW and skip-gram in DeepWalk. A 75% goal is an implementation of DeepWalk using CBOW. A 125% goal is a way to further improve DeepWalk or a generally better algorithm to learn graphical representations.

## Milestones

# 1st Technical Milestone for 15-300

Implement CBOW, train it on a middle-sized dataset, and compare the result to reference implementation or word embedding

# Bi-weekly Milestones for 15-400

February 1st: implement skip-gram, train it on a middle-sized dataset, and compare the result to reference implementation or word embedding

February 15th: train CBOW and skip-gram on large datasets and compare the results

March 1st: modify CBOW to fit into DeepWalk

March 22nd: train the modified DeepWalk on a middle-sized dataset

April 5th: train the modified DeepWalk on large datasets used in the paper and compare the results

April 19th: detailed analysis on the differences in several aspects presented in the paper

May 3nd: explore other ways to improve DeepWalk based on the analysis or other algorithms to learn graph representations, or make similar modifications on related papers, write final report

## Literature Search

I have collected two papers [1], [2] about word2vec, which include the description of CBOW and skip-gram. I have also collected the paper about DeepWalk [3]. These are the papers that I need to start with, and I may find other papers during the research.

## Resources Needed
In terms of code, I will need the reference code for CBOW, skip-gram, and the starter code for DeepWalk. There are many open source implementations of CBOW and skip-gram, and the authors of the DeepWalk paper have also open-sourced their code. In terms of hardware, I will start with a small amount of data that can be processed locally on my MacBook Pro. I also have an Alienware with a 8th-gen 6-core Intel i7 CPU and an Nvidia GeForce GTX 1070 GPU, which is able to deal with middle-sized data. For larger data I will talk with Professor Yiming Yang and Yuexin Wu and see what machines they use. In terms of data, there are many open source datasets of graphs such as social networks.

## Reference 

1. Mikolov, Tomas et al. “Efficient Estimation of Word Representations in Vector Space.” CoRR abs/1301.3781 (2013): n. Pag.
2. Mikolov, Tomas et al. “Distributed Representations of Words and Phrases and their Compositionality.” NIPS (2013).
3. Perozzi, Bryan et al. “DeepWalk: Online Learning of Social Representations.” KDD(2014).



