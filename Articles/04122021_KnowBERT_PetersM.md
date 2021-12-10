```

---

title: Knowledge Enhanced Contextual word Representations  author: Matthew E. Peters, Mark Neumann, Robert L. Logan IV, Roy Schwartz, Vidur Joshi, Sameer Singh, Noah A. Smith... date: 2019 ARXIV : https://arxiv.org/abs/1909.04164 

---

``` 

# Knowledge Enhanced Contextual word Representations   

## ABTRACT

 Contextual word representations, typically trained on unstructured, unlabeled text, do not contain any explicit **grounding to real world entities** and are often **unable to remember facts** about those entities. We propose a general method to embed multiple knowledge bases (KBs) into large scale models, and thereby enhance their representations with structured, human-curated knowledge. For each KB, we first use an integrated entity linker to retrieve relevant entity embeddings, then update contextual word representations via a form of word-to-entity attention. In contrast to previous approaches, the entity linkers and self-supervised language modeling objective are jointly trained end-to-end in a multitask setting that combines a small amount of entity linking supervision with a large amount of raw text. After integrating WordNet and a subset of Wikipedia into BERT, the knowledge enhanced BERT (KnowBert) demonstrates improved perplexity, ability to recall facts as measured in a probing task and downstream performance on relationship extraction, entity typing, and word sense disambiguation. KnowBert's runtime is comparable to BERT's and it scales to large KBs. 

 ## Brief notes 

- multiple KB integration in BERT embeddings 
-  Entity Linker + contextual representation with a joint training step on large raw text - Integration of WordNet and a Wikipedia subset in BERT  - Improved perplexity / Disambiguation

 ## 1. Related work

* Contextual word embeddings 
* Entity embeddings  
*  continuous vector representation   
*  knowledge graph-based method that score of observed triples in KB    
  *  2 cat : translational distance models  (TransE) VS linear model (TuckER )    
*  model use : [**TuckER**](https://arxiv.org/abs/1901.09590) embeddings aggregator   
  * ​	 here a benchmark about it : https://arxiv.org/pdf/2003.08001.pdf  
*  other models : entity metadata . entity context, entity context and KB  
* agnostic approach 
* Entity-aware models: adding KB to generative models but need to be annotated 
*  Task specific KB archi : position : generally transferable representation 

## 2. KnowBert 

* Bert extension  but could be applied to other ML archi
*  No assumption about entity type 
* KB included : Wordnet (graph+synset def) and Wikipedia (page embeddings) 
*  Need a entity candidate selector :  input text / output list of candidates with indexed spans and prior proba 
*  Fix number of candidate 30 / rule based selection 
*  KnowBert runtime independent to KB size 

 ### 2.1. The Knowledge Attention and Recontextualization  the KAR component   

input : contextual representation of a layer output : enhanced KB representation 

STEPS : 

* Mention-span repres : Transformer vectors with linear projection : Hproj
* Entity linker : MLP block  using candidates list embeddings and prior // if supervision EL possible computing a loss with gold entity E 
*  Knowledge enhanced entity-span repres : normalisation of mention-span repres and pruning candidate list / entity weighted embedding combination update S' 
*  Recontextualisation : multihead self-attention costum  
*  Alignment of BERT and entity vectors   

  Training process : "chain-thaw" process and fine-tuning of network  by minimizing loss aggreg of BERT and EL models

 The entity embedding and candidates selection help masked LM to predict easily

 ## 2.2. Experiments details 

KnowBERT-wiki : 

* entity selector of Ganea and Hofman 2017 : CrossWikis  Stats about Wiki / Web corpus and Yago 
*  Entity-embedding : skip-gram objective  
*  Wikipedia title embeddings : no graph structure  because [BigGraph](https://github.com/facebookresearch/PyTorch-BigGraph) demonstrate that no value is added with relationnal data 
*  supervision with AIDA-CoNLL dataset

 Know BERT-wordnet : 

* combination of synset meta data . lemma metadata . relational metadata and relational graph
* ruled-based lemmatizer without POS 
*  graph and synset because of proff of added value of synset 
* Use of  [SoTA sentence embedding vector](https://arxiv.org/abs/1804.00079) concatanated with TuckER 
*  supervision with SemCor WSD dataset  

Know BERT-wordnet-wiki : both 

Eval : perplexity / factual recall 

Downstream tasks :  Relation extraction / Word in context (dual exemple with sense comparison) / Entity typing 

## 3. Results and conclusions Experiments : 

Relation extraction : better for TARCRED but not for SemEval 2010 

* WiC : better 

* Entity typing : little improvement 

 Conclusions : 

* Efficient and general model 
*  Improve hability to recall facts and quality of masked LM

 Perspectives : extending KB incorporation 
