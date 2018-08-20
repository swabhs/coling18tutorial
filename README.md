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

* Apoorv Agarwal, Sriramkumar Balasubramanian, Anup Kotalwar, Jiehan Zheng, and Owen Ram- bow. Frame semantic tree kernels for social network extraction from text. In Proc. of EACL, 2014.
* Waleed Ammar, George Mulcaire, Yulia Tsvetkov, Guillaume Lample, Chris Dyer, and Noah A Smith. Massively multilingual word embeddings, 2016. arXiv:1602.01925.
* Collin Baker, Michael Ellsworth, and Katrin Erk. SemEval’07 Task 19: Frame semantic structure extraction. In Proc. of SemEval, 2007.
* Laura Banarescu, Claire Bonial, Shu Cai, Madalina Georgescu, Kira Griffitt, Ulf Hermjakob, Kevin Knight, Philipp Koehn, Martha Palmer, and Nathan Schneider. Abstract meaning representation for sembanking. In Proc. of Linguistic Annotation Workshop and Interoperability with Discourse, 2013.
* Teresa Botschen, Iryna Gurevych, Jan-Christoph Klie, Hatem Mousselly Sergieh, and Stefan Roth. Multimodal frame identification with multilingual evaluation. In Proc. of ACL, 2018.
* Aljoscha Burchardt and Anette Frank. Approaching textual entailment with lfg and framenet frames. In Proc. of PASCAL RTE Challenge Workshop. Citeseer, 2006.
* Xavier Carreras and Llu ́ıs Ma`rquez. Introduction to the CoNLL-2005 shared task: Semantic role labeling. In Proc. of CoNLL, 2005.
* Yun-Nung Chen, William Yang Wang, and Alexander I Rudnicky. Unsupervised induction and filling of semantic slots for spoken dialogue systems using frame-semantic parsing. In Proc. of ASRU-IEEE, 2013.
* Bob Coyne, Alex Klapheke, Masoud Rouhizadeh, Richard Sproat, and Daniel Bauer. Annotation tools and knowledge representation for a text-to-scene system. In Proc. of COLING, 2012.
* Dipanjan Das, Andre ́ F. T. Martins, and Noah A. Smith. An exact dual decomposition algorithm for shallow semantic parsing with constraints. In Proc. of *SEM, 2012. URL http://dl.acm.org/citation.cfm?id=2387636.2387671.
* Dipanjan Das, Desai Chen, Andre ́ FT Martins, Nathan Schneider, and Noah A Smith. Frame- semantic parsing. Computational linguistics, 40(1):9–56, 2014.
* David Dowty. Thematic proto-roles and argument selection. language, 67(3):547–619, 1991.
* Nicholas FitzGerald, Oscar Ta ̈ckstro ̈m, Kuzman Ganchev, and Dipanjan Das. Semantic role labeling
with neural network factors. In Proc. of EMNLP, 2015.
* Nicholas FitzGerald, Julian Michael, Luheng He, and Luke Zettlemoyer. Large-scale qa-srl parsing. In Proc. of ACL, 2018.
* Hagen Fürstenau and Mirella Lapata. Semi-supervised semantic role labeling via structural align- ment. Computational Linguistics, 38(1):135–171, 2012.
* Daniel Gildea and Daniel Jurafsky. Automatic labeling of semantic roles. Computational Linguis- tics, 28(3):245–288, 2002.
* Jesu ́s Gime ́nez and Llu ́ıs Ma`rquez. Linguistic features for automatic evaluation of heterogenous mt systems. In Proc. of Workshop on SMT, pp. 256–264. Association for Computational Linguistics, 2007.
* Jan Hajič, Massimiliano Ciaramita, Richard Johansson, Daisuke Kawahara, Maria Antònia Martí, Llu ́ıs Ma`rquez, Adam Meyers, Joakim Nivre, Sebastian Pado ́, Jan Sˇteˇpa ́nek, Pavel Stranˇa ́k, Mihai Surdeanu, Nianwen Xue, and Yi Zhang. The CoNLL-2009 shared task: Syntactic and semantic dependencies in multiple languages. In Proc. of CoNLL, 2009.
* Silvana Hartmann, Ilia Kuznetsov, Teresa Martin, and Iryna Gurevych. Out-of-domain framenet semantic role labeling. In Proc. of EACL, 2017.
* Luheng He, Mike Lewis, and Luke Zettlemoyer. Question-answer driven semantic role labeling: Using natural language to annotate natural language. In Proc. of EMNLP, 2015.
* Luheng He, Kenton Lee, Mike Lewis, and Luke Zettlemoyer. Deep semantic role labeling: What works and what’s next. In Proc. of ACL, 2017.
* Luheng He, Kenton Lee, Omer Levy, and Luke Zettlemoyer. Jointly predicting predicates and arguments in neural semantic role labeling. 2018.
* Karl Moritz Hermann, Dipanjan Das, Jason Weston, and Kuzman Ganchev. Semantic frame identi- fication with distributed word representations. In Proc. of ACL, 2014.
* Anders Johannsen, He ́ctor Mart ́ınez Alonso, and Anders Søgaard. Any-language frame-semantic parsing. In Proc. of EMNLP, pp. 2062–2066, 2015.
* Richard Johansson and Pierre Nugues. LTH: Semantic structure extraction using nonprojective dependency trees. In Proc. of SemEval, 2007. URL http://dl.acm.org/citation.cfm?id=1621474.1621522.
* Richard Johansson and Pierre Nugues. Dependency-based syntactic-semantic analysis with Prop- Bank and NomBank. In Proc. of CoNLL, 2008.
* Paul Kingsbury and Martha Palmer. From treebank to propbank. In Proc. of LREC, 2002.
* Meghana Kshirsagar, Sam Thomson, Nathan Schneider, Jaime Carbonell, Noah A Smith, and Chris Dyer. Frame-semantic role labeling with heterogeneous annotations. In Proc. of NAACL, 2015.
* Xavier Llu ́ıs and Llu ́ıs Ma`rquez. A joint model for parsing syntactic and semantic dependencies. In
Proc. of CoNLL, 2008.
* Xavier Llu ́ıs, Xavier Carreras, and Llu ́ıs Ma`rquez. Joint arc-factored parsing of syntactic and se-
mantic dependencies. Transactions of the ACL, 1:219–230, 2013.
* Thang Luong, Hieu Pham, and Christopher D Manning. Bilingual word representations with mono-
lingual quality in mind. In Proc. of Workshop of VSM in NLP, pp. 151–159, 2015.
* Diego Marcheggiani, Joost Bastings, and Ivan Titov. Exploiting semantics in neural machine trans-
lation with graph convolutional networks. In Proc. of NAACL, 2018.
* Alessandro Moschitti. Kernel methods, syntax and semantics for relational text categorization. In
Proc. of CIKM, pp. 253–262. ACM, 2008.
* Alessandro Moschitti, Silvia Quarteroni, Roberto Basili, and Suresh Manandhar. Exploiting syntac- tic and shallow semantic kernels for question answer classification. In Proc. of ACL, pp. 776–783, 2007.
* Phoebe Mulcaire, Swabha Swayamdipta, and Noah Smith. Polyglot semantic role labeling. In Proc. of ACL, 2018.
* Srini Narayanan and Sanda Harabagiu. Question answering based on semantic structures. In Proc. of ICCL, pp. 693. Association for Computational Linguistics, 2004.
* Sebastian Padó and Mirella Lapata. Cross-lingual annotation projection for semantic roles. Journal of Artificial Intelligence Research, 36:307–340, 2009.
* Martha Palmer, Daniel Gildea, and Paul Kingsbury. The Proposition Bank: An annotated corpus of semantic roles. Computational Linguistics, 31(1):71–106, 2005.
* Ellie Pavlick, Travis Wolfe, Pushpendre Rastogi, Chris Callison-Burch, Mark Dredze, and Benjamin Van Durme. Framenet+: Fast paraphrastic tripling of framenet. In Proc. of ACL, volume 2, pp. 408–413, 2015.
* Hao Peng, Sam Thomson, Swabha Swayamdipta, and Noah A. Smith. Learning joint seman- tic parsers from disjoint data, 2018. URL https://arxiv.org/abs/1804.05990. arXiv:1804.05990.
* Pushpendre Rastogi and Benjamin Van Durme. Augmenting framenet via ppdb. In Proc. of Work- shop on EVENTS, 2014.
* Drew Reisinger, Rachel Rudinger, Francis Ferraro, Craig Harman, Kyle Rawlins, and Benjamin Van Durme. Semantic proto-roles. Transactions of the Association for Computational Linguistics, 3:475–488, 2015.
* Michael Roth and Mirella Lapata. Neural semantic role labeling with dependency path embeddings, 2016. arXiv:1605.07515.
* Dan Shen and Mirella Lapata. Using semantic roles to improve question answering. In Proc. of EMNLP-CoNLL, 2007.
* Anders Søgaard, Barbara Plank, and Hector Martinez Alonso. Using frame semantics for knowledge extraction from twitter. In Proc. of AAAI, 2015.
* Emma Strubell, Patrick Verga, Daniel Andor, David Weiss, and Andrew McCallum. Linguistically- informed self-attention for semantic role labeling, 2018. URL http://arxiv.org/abs/1804.08199. arXiv:1804.08199.
* Mihai Surdeanu, Sanda Harabagiu, John Williams, and Paul Aarseth. Using predicate-argument structures for information extraction. In Proc. of ACL, 2003. doi: 10.3115/1075096.1075098. URL https://doi.org/10.3115/1075096.1075098.
* Mihai Surdeanu, Richard Johansson, Adam Meyers, Llu ́ıs Ma`rquez, and Joakim Nivre. The CoNLL- 2008 shared task on joint parsing of syntactic and semantic dependencies. In Proc. of CoNLL, 2008.
* Swabha Swayamdipta, Miguel Ballesteros, Chris Dyer, and Noah A. Smith. Greedy, joint syntactic- semantic parsing with Stack LSTMs. In Proc. of CoNLL, 2016.
* Swabha Swayamdipta, Sam Thomson, Chris Dyer, and Noah A. Smith. Frame-semantic parsing with softmax-margin segmental rnns and a syntactic scaffold, 2017. URL http://arxiv.org/abs/1706.09528. arXiv:1706.09528.
* Zhixing Tan, Mingxuan Wang, Jun Xie, Yidong Chen, and Xiaodong Shi. Deep semantic role labeling with self-attention. In Proc. of AAAI, 2018.
* Marta Tatu and Dan Moldovan. A semantic approach to recognizing textual entailment. In Proc. of EMNLP, pp. 371–378. Association for Computational Linguistics, 2005.
* Ivan Titov and Alexandre Klementiev. A bayesian approach to unsupervised semantic role induction. In Proc. of EACL, 2012.
* Ivan Titov, James Henderson, Paola Merlo, and Gabriele Musillo. Online graph planarisation for synchronous parsing of semantic and syntactic dependencies. In Proc. of IJCAI, 2009.
* Kristina Toutanova, Aria Haghighi, and Christopher D. Manning. A global joint model for semantic role labeling. Computational Linguistics, 34(2):161–191, 2008.
* Dekai Wu and Pascale Fung. Semantic roles for smt: a hybrid two-pass model. In Proc. of ACL, pp. 13–16. Association for Computational Linguistics, 2009.
* Bishan Yang and Tom Mitchell. A joint sequential and relational model for frame-semantic parsing. In Proc. of EMNLP, 2017.
* Jie Zhou and Wei Xu. End-to-end learning of semantic role labeling using recurrent neural networks. In Proc. of ACL, 2015.