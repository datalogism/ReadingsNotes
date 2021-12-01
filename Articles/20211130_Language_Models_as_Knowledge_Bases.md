```
---
title: Language Models as Knowledge Bases?
author: Fabio Petroni, Tim Rocktäschel, Patrick Lewis, Anton Bakhtin, Yuxiang Wu, Alexander H. Miller, Sebastian Riedel
date: sept 2019
arxiv : https://arxiv.org/abs/1909.01066
---
```

# Language Models as Knowledge Bases?

## ABTRACT

Recent progress in pretraining language models on large textual corpora led to a surge of improvements for downstream NLP tasks. Whilst learning linguistic knowledge, these models may also be storing relational knowledge present in the training data, and may be able to answer queries structured as "fill-in-the-blank" cloze statements. Language models have many advantages over structured knowledge bases: they require no schema engineering, allow practitioners to query about an open class of relations, are easy to extend to more data, and require no human supervision to train. We present an in-depth analysis of the relational knowledge already present (without fine-tuning) in a wide range of state-of-the-art pretrained language models. We find that (i) without fine-tuning, BERT contains relational knowledge competitive with traditional NLP methods that have some access to oracle knowledge, (ii) BERT also does remarkably well on open-domain question answering against a supervised baseline, and (iii) certain types of factual knowledge are learned much more readily than others by standard language model pretraining approaches. The surprisingly strong ability of these models to recall factual knowledge without any fine-tuning demonstrates their potential as unsupervised open-domain QA systems. The code to reproduce our analysis is available at [this https URL](https://github.com/facebookresearch/LAMA).     

## Brief notes

* Language model are storing relational knowledges present in training data, due to the "fill the blank" process.
* Advantages :
  * no schema
  * open class relation
  * no supervision to train it
  * easy to extend

* BERT without fine tuning can :
  * open question relational 
  * learn factual knowledges
* BERT and Elmo are optimized for : predictiong next words / predicting masked words
* Knowledge base : effective for accessing annotated gold standard data with queries BUT not easy to extract relation from text
  * Need of complex NLP process : entity extraction / coreference resolution / entity linking / relation extraction
  * Need also training data and fixed schema 

As LM as a big potential of represent relational data... Questions :

*  How much relational knowledge do they store ?
* How does this from different types of knowledges ? common senses / QA / fact about entities 
* How do their perform comparative to symbolic automatically extracted text ?

The LAMA probe experiment : facts knowledge bases VS LM : 

* KB : TREX (wikidata triples based), ConceptNET (multilingual kb of commonsense relationships), SQUAD (QA dataset)
* LM : fairseq-fconv (multiple gated conv trained on WikiText), Transformer XL, BERT, ELMO

Results :

* BERT capture same level of info than KB  on theses examples
* LM Not really good on N-to-M relations
* BERT is the better model and get respectfull performances on open-domain QA 



