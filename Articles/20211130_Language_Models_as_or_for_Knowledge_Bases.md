```
---
title: Language Models as or for Knowledge Bases?
author: Simon Razniewski, Andrew Yates, Nora Kassner, Gerhard Weikum
date: Oct 2021
arxiv : https://arxiv.org/abs/2110.04888
---
```

# Language Models as or For Knowledge Bases?

## ABTRACT

Pre-trained language models (LMs) have recently gained attention for their potential as an alternative to (or proxy for) explicit knowledge bases (KBs). In this position paper, we examine this hypothesis, identify strengths and limitations of both LMs and KBs, and discuss the complementary nature of the two paradigms. In particular, we offer qualitative arguments that latent LMs are not suitable as a substitute for explicit KBs, but could play a major role for augmenting and curating KBs.     

## Brief notes

* A summary of state of art concerning the LM as KB question

* Intrinsic consideration :

  * Prediction VS lookup :
    * KB explicitly be looked up
    * LM based on moving probabilities : not possible to directly enumerate KG inside
  * Statistical correlation VS explicit KNG :
    * semantic biais of LM due to frequent values and co-occurences
  * Being aware of the limits :
    * KB easy to assert if not fact no answer
    * LM will try to find in any way an answer
  * Coverage : 
    * KB limited by by a set of predicates
    * LM could find non standard relations
  * Curability :
    * correcting a KB is possible
    * LM need to be retrained
  * Provenance : LM give us no traceability

* Pragmatic consideration :

  * entity disambuigation : LM mix differents sources of info without tracibility / KB not able to answer to disambiguation pb alone but give us tracibility
  * numbers and singleton : LM ok for discrete values but not with others 
  * subject with zero or many objects : how to use the LM given answers ?

  CONCLUSIONS :

  The great potential of LM > KB curation (main pitfall of it)

  for KB augmentation in same way than KG embeddings but give complementary evidence 

  Lm allows us to use text corpora BUt need to give confident support 

  LM for predicting assertions 

