--- 
layout: page 
title: "MR 2/6/19"
---

## Major Changes
No major changes encountered or expected. The ultimate goal is to improve DeepWalk and potentially other graph representation learning algorithms. However, as discussed below, as I learned more about the model and since I’m ahead of schedule, I will explore other methods to improve the model.

## What I Have Accomplished
I have read the Word2Vec papers and the DeepWalk paper thoroughly, implemented CBOW, and changed Skip-Gram to CBOW in DeepWalk. Now the Skip-Gram version of DeepWalk compiles and runs, but there are some issues with the testing script, so I don’t know the accuracy and whether there are bugs in my implementation. I’m currently working on the testing script.

## Meeting My Milestone
I met my milestone and accomplished more than I anticipated.

## Surprises
No major surprised encountered.

## Looking Ahead
I will fix the testing script and the potential bugs in my CBOW implementation.

## Revisions to My Future Milestones
As I learned more about the model from the papers I read, I discovered that there are more possible improvements such as negative sampling and change of loss function. Since I’m ahead of my schedule, I will try to explore those improvements as well in the future.

## Resources Needed
Right now I’m using my gaming laptop to do all the training, which works fine (takes a few minutes on a reasonably large dataset). I’m not planning to train on extremely large datasets, so computational power is not an issue. As for the datasets, I have found a few of them meeting the general requirements (labeled, etc.), but the training and testing scripts only accept a very specific format of input, and I only have one dataset in that format. So I will probably have to spend some time on changing the format of input to meet the requirements.

