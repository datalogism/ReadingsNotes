```
---
title: REBEL: Relation Extraction By End-to-end Language generation
author:Pere-Lluís Huguet Cabot, Roberto Navigli
date: Nov 2021
link : https://aclanthology.org/2021.findings-emnlp.204/
---
```

# REBEL: Relation Extraction By End-to-end Language generation

## ABTRACT
Generative commonsense reasoning which aims to empower machines to generate sentences with the capacity of reasoning over a set of concepts is a critical bottleneck for text generation. Even the state-of-the-art pre-trained language generation models struggle at this task and often produce implausible and anomalous sentences. One reason is that they rarely consider incorporating the knowledge graph which can provide rich relational information among the commonsense concepts. To promote the ability of commonsense reasoning for text generation, we propose a novel knowledge graph augmented pre-trained language generation model KG-BART, which encompasses the complex relations of concepts through the knowledge graph and produces more logical and natural sentences as output. Moreover, KG-BART can leverage the graph attention to aggregate the rich concept semantics that enhances the model generalization on unseen concept sets. Experiments on benchmark CommonGen dataset verify the effectiveness of our proposed approach by comparing with several strong pre-trained language generation models, particularly KG-BART outperforms BART by 5.80, 4.60, in terms of BLEU-3, 4. Moreover, we also show that the generated context by our model can work as background scenarios to benefit downstream commonsense QA tasks. 

## Intro and context

Rebel is a seq2seq model based on BART that allows end-to-end relation extraction

Traditionally we split the task into two sub-task :

* NER extraction

* Relation extraction classification

  with LSTM / CNN 

  Transformer respresentation 

  Try to learn it by jointly training NER and RC.

  But have some withdraws : 
  The seq2seq models offer off-the-shelf solutions that overcomes some issues as : predicting relations incompatibles together.  

BART / T5 performs already prove their effectivness on : 

* Entity linking pb 
* AMR parsing
* Semantic Role labelling
* word sence disambiguation

Open to unseen entities !

## The REBEL model

BART-Large as base model

using the translation task training 

input : sentence with entities  / set of triplets of relation

Triplet linearisation reversble process for enabling relations in text  : minimise nb of token encoded

sort triplet by order of appaerance

Transform set of relations into text sequence

## DATASET 

* REBEL dataset : 

  based on t-REX : DBpedia abstracts & NER annotation

  * Use an "old entity tool" > Spotlight (2012 Daiber) 
  * supposed the presence of the relations in text

  -> Wikipedia  (via wikiextractor) + Wikidata (via wikimapper)

   could be processed for other lang / wikidump

  pb : could be noisy 

  solution : using Roberta trained for NLI (natural lang inference) :

  * Filter relation not in text
  * Keep relation with pred perf > 75%
  * random split

  220 relations 

* Others datasets :

  |                 | CONLL04        | DocRed    | NYT                      | ADE        | Re-tacred     |
  | --------------- | -------------- | --------- | ------------------------ | ---------- | ------------- |
  | source          | twitter / news | Wikipedia | News articles + Freebase | biomedical | news / web    |
  | annotation      | manually       | Wikidata  | Freebase                 | manually   | crowdsourcing |
  | nb rel type     | 4              | 96        | 24                       | 1          | 41            |
  | nb entity types | 4              | 6         | 3                        | ?          | 23            |
  |                 |                |           |                          |            |               |

  ## RESULTS

  relation extraction :

  better than NER+RC systems

  Every methods is not really good on DocRed dataset

  less learning effort for good perf

  the pre-training importance

  open to be fine-tuned with new datasets

  relation classification :

  Almost same perf

  

  ## CONCLUSIONS 

  flexible 

  open to new domain

  dataset creation pipeline

  Really usefull for tracking Wikipedia changes.

  

