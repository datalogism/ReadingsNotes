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
Extracting relation triplets from raw text is a crucial task in Information Extraction, en- abling multiple applications such as populat- ing or validating knowledge bases, factcheck- ing, and other downstream tasks. However, it usually involves multiple-step pipelines that propagate errors or are limited to a small num- ber of relation types. To overcome these is- sues, we propose the use of autoregressive seq2seq models. Such models have previously been shown to perform well not only in lan- guage generation, but also in NLU tasks such as Entity Linking, thanks to their framing as seq2seq tasks. In this paper, we show how Relation Extraction can be simplified by ex- pressing triplets as a sequence of text and we present REBEL, a seq2seq model based on BART that performs end-to-end relation ex- traction for more than **200 different relation types**. We show our model’s flexibility by **fine- tuning it on an array of Relation Extraction and Relation Classification benchmarks**, with it at- taining state-of-the-art performance in most of them.

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

* Must be fine tuned on relation extraction task and relation classification (with few epochs)

Based on BART-Large 

using the translation task training 

> input : sentence with entities  
> transling it into a set of triples that refers to relations (that can not appears in the sentences)

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

  

