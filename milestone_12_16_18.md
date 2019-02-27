--- 
layout: page 
title: "MR 12/16"
---

## Major Changes
There are no major changes. There is one extension: besides DeepWalk, I have discovered later state-of-the-art graph representation/embedding algorithms such as node2vec that also use NLP algorithms (Skip Gram), so I plan to try replacing them by CBOW as well.

## What I Have Accomplished So Far
I have implemented CBOW in C++ and tested it on a small dataset. My teammate and I have also parallelized DeepWalk with Skip Gram (the original version) using OpenMP and SIMD operations and achieved 6x speedup with 12-thread CPU. I met the milestone I described in my original project proposal.

## Surprises
A surprise is that DeepWalk is hard to parallelize. The paper claims scalability and linear speedup, but the authors have removed the multiprocessing code from github, and other implementations shows that the speedup is far from linear. Good news is that my teammates and I have doubled the speedup to 6x on 12-thread CPU from a highly optimized parallel implementation using OpenMP and SIMD operations. Also training does not take too long on datasets of considerable size (~40s on graph with |V|=4039, |E|=88234, ~100s on grah with |V|=10312, |E|=333983).

## Revisions to my 15-400 Milestones
The current goal is very clear and I think I am on the right track and making progress. For later goals, as stated above, I have discovered other algorithms using Skip Gram, so I should be able to apply my work to them as well. This is more like a complement or an extension than a revision to my milestones. I do not have other revisions other than this at this point.

## Resources Needed
I have all the resources I need. The DeepWalk paper provides a detailed benchmark. I have collected the Blogcatalog, Flickr, and Youtube labeled network datasets used in the paper and some more. I have access to machines with high computational power.
