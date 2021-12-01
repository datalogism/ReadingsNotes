```
---
title: Can Knowledge Graph Embeddings Tell Us What Fact-checked Claims Are About? 
author: Valentina Beretta, Katarina Boland, Luke Lo Seen, Sébastien Harispe, Konstantin Todorov, et al..
date: 2020
DOI : 10.18653/v1/2020.insights-1.11
HAL : https://hal.archives-ouvertes.fr/hal-02986882/
---
```

# Can Knowledge Graph Embeddings Tell Us What Fact-checked Claims Are About? 

## ABTRACT

The web offers a wealth of discourse data that help researchers from various fields analyze debates about current societal issues and gauge the effects on society of important phenomena such as misinformation spread. Such analyses often revolve around claims made by people about a given topic of interest. Fact-checking portals offer partially structured information that can assist such analysis. However, exploiting the network structure of such online discourse data is as of yet under-explored. We study the effectiveness of using neural-graph embedding features for claim topic prediction and their complementarity with text em- beddings. We show that graph embeddings are modestly complementary with text embed- dings, but the low performance of graph em- bedding features alone indicate that the model fails to capture topological features pertinent of the topic prediction task.

## Brief notes

A complex KB graph : ClaimsKG . Claims are linked to Reviews (headline/mention/entity), metadata (author/date/text), Keywords (that are linked to Topics). Topics is in fact shared by a number of KW

small dataset !



* Task :  multi-label topic prediction via representation learning of text AND graph together for :
  * entity linking
  * link prediction (for KG completion/fusion)

* Pipeline : 
  * Graph embedding model :  CANDECOM/PARAFAC canonical decomposition with n3 regularisation 
  * feature fusion : SOTA unsupervised method fusion with text emedding in DistillRoberta and GPT2

* Evaluation : MRR and Hit@k metrics

* Result :
  *  not efficient with KGE ...
  * not  able to manage part of complex structure : problem of equivalance of clique of claims/kwd/topic
  * higly depends of size of dataset
  * must use model that capture transitive/ reflexive/ anti-symetric relation 
  * Graph neural network ? Random Walk approaches ?

