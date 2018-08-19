# COLING 2018 Tutorial on Multilingual FrameNet: Automatic semantic role labeling for FrameNet

This repository contains the materials to be taught in the **Automatic Semantic Role Labeling for FrameNet** section of the [tutorial on Multilingual FrameNet](https://framenet.icsi.berkeley.edu/fndrupal/node/5552/) at [COLING 2018](https://coling2018.org/), to be presented by [Swabha Swayamdipta](http://cs.cmu.edu/~sswayamd/).

## Slides

[**Automatic SRL for FrameNet**](https://github.com/Noahs-ARK/coling18tutorial/blob/master/Slides-Swabha.pdf).

[**Full tutorial Slides (early draft)**](https://framenet2.icsi.berkeley.edu/docs/allslides.pdf).

## Abstract

A variety of semantic role labeling systems have been trained on the English FrameNet data to automatically create representations similar to manual annotations (Swayamdipta et al. 2017; Das et al. 2014); the tutorial will discuss the state of the art in automatic frame semantic role labeling for English and the prospects for similar systems for other languages.



## Overview of tutorial section

In this section, we will be discussing machine learning approaches to automatically predict frame-semantic graphs from sentences. This task is formally called frame-semantic role labeling. Semantic role labeling is a structured prediction task which maps a sentence to a graph. The nodes in the graph could either be targets (or predicates), words or phrases in the sentence realized as frame elements or arguments. Targets are additionally annotated with their corresponding lexical unit and evoked frame. Words in the sentence which are neither targets nor frame elements exist as disconnected nodes in the graph. Edges in the graph join targets with their arguments, and hence correspond to frame element labels.

Traditionally, approaches for semantic role labeling treat the problem as a sequence of classification decisions - target identification, followed by frame identification and then by argument identification. It is typical to consider each target independently of other targets in the sentence. Most recent approaches employ variants of joint and multitask learning to improve on those earlier methods, by leveraging additional signals in the data, or external, complementary resources.
Syntactic features often guide SRL models - these involve syntactic substructures, such as part of speech tags, constituent phrase types, syntactic path from target to argument, etc. Inference involves global consistency enforcement for each of the classification decisions.
Approaches involving greedy search, integer linear programming as well as dynamic programming for inference have been employed to varying degrees of success.

Modern approaches rely on neural architectures to learn representations for nodes and edges in the graph. While recurrent neural nets have been very successful by virtue of encoding a long context, feedforward and convolutional nets have also demonstrated benefits.
Some neural approaches do not employ any syntactic input whatsoever for semantic role labeling.
While these still perform well, it has been shown that incorporating syntactic constraints and biases further improves performance.

Most of the automatic SRL efforts have focused on English, however. The challenges outlining automatic SRL in other languages include lack of large training corpora (even though there have been efforts on several languages) and a lack of high performing syntactic parsers in those languages, to name a few. However, with a multilingual FrameNet, there is a lot of potential in designing models which can be adapted cross lingually. These models could be trained on one language and transfer to others, with a certain level of adaptation at the input sentence level. Models could also be trained jointly on several languages. Applications of a multilingual frame-SRL model could include language-independent question answering, information extraction and relation extraction, among others.

## References

TBD
