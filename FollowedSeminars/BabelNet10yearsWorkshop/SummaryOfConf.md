# Workshop on Ten Years of BabelNet and Multilingual Neurosymbolic Natural Language Understanding

http://mousse-project.org/events/event-a5f3r5.html


## PROGRAMME

### DAY 1 

* Ten Years of BabelNet: Opening - Roberto Navigli
* Lexicography in the Age of Concept - Simon Krek X
* Progress in defining NLU in specifically reading comprehension "skills" - Anna ROgers X
* BabelNet and Discourse Semantics - Bonnie Webber
* ID10M: Idiom Identification in 10 Languages
* Large Language Models: Will they keep getting bigger? And, how will we use them if they do? - Luke Zettlemoyer X
* Probing for Predicate Argument Structures in Pretrained Language Models - Simone Conia
* Redesigning WSD with Extractive Sense Comprehension and Continuous Sense Comprehension - Edoardo Barba X
* On the complementarity of neural and symbolic approaches, and on how to transfer between them - Eduard Hovy X
* What do neural vs neurosymbolic models learn? - Hinrich Schütze

### DAY 2 

* Summary of the first day - Roberto Navigli X
* Neurosymbolic semantic parsing - Alexander Koller X
* Distilling conceptual knowledge from BERT - Steven Schockaert X
* REBEL: Relation Extraction By End-to-end Language generation - Pere-Lluís Huguet Cabot X
* Unifying verb-based resources into an event-type ontology -Jan Hajič
* Wrap-up and closing session - Roberto Navigli

--- 

## DAY 1

### 1. Lexicography in the Age of Concept - Simon Krek

* Simon Krek page : https://www.simonkrek.si/en/

* Linguistic LOD Cloud 
* UE investment on project
* Word Atlas > Babel will integrate new dictionnary : classicals (Larousse for ex.) and specialized (UMLS/HCtop)
* A network of linked synset
* Could be used for following tasks :
  * Multi entity disambiguation
  * Semantic role labelling
  * Commonsense mining
  * Reasoning
 Language independent => Umberto Eco Blackwell and the perfect language
 
 => Lexicography impossible mission : defining word sens
 
 Exemple of the synset of Love 
 How to anotating meaning from text ? 


### 2. Multilingual Neurosymbolic NLU  - Anna Rogers

=> Closer paper : [2020- Getting Closer to AI Complete Question Answering: A Set of Prerequisite Real Tasks(https://ojs.aaai.org/index.php/AAAI/article/download/6398/6254)

* We are living a NLP evaluation crisis : exemple of benchmark of QA task
* How to define a NLP task for human ?

> " Wikitionnary have a wired view on things"

* Interresting papers of Anna ROgers :
 * [2021 - BERT Busters: Outlier Dimensions that Disrupt Transformers](https://aclanthology.org/2021.findings-acl.300/)
 * [2022 - A Primer in BERTology: What We Know About How BERT Works](https://watermark.silverchair.com/tacl_a_00349.pdf?token=AQECAHi208BE49Ooan9kkhW_Ercy7Dm3ZL_9Cf3qfKAc485ysgAAAugwggLkBgkqhkiG9w0BBwagggLVMIIC0QIBADCCAsoGCSqGSIb3DQEHATAeBglghkgBZQMEAS4wEQQM5CY_e_4ZG9ZQGShNAgEQgIICmxN1zN-d4IUQblCFBGAQTmqfRX47glTSLBQLTajW20FdMwFR3GJS6SiZyJwIx_prcxs4pyuFkToaPWFg4fbVfWySfkmBY_blp0SEXiqBvJpvtM0UT-F65ah8bvI3SOU91LxavihLsissHNwazeT0BNqDogGW9RrV68juCDIJ1N_T7KsopjbIZ2TH06J_nAlGes59JuWDublW7OemQlexZ3RWMXqmEKzk6hOZ8cat5Z8KtR5_ydo1XsSPXLBrTeDVwioySdmMwnKDz1yffbhTMT69ltGKQB6iN0FB7NcWBHrFy-zqOQNoLNZWyheRHsm7T9OCJeNTP1QYRlG8zjT7sRt1IXSYBGIb_KjN3qmITcluc-b_0_fdZlZJ2X35OhEEGu-2uLmDfuqN79wde8jeSI10xfxu9ic-BvDGdsFoFL4BIT4FY9Q0Z-0lAsTLMJon4dvHfQWnDAGARaSlJSN3-7knnu4x3iD1gB0id9a3fs5KsQgrxmhpP4u1M23NcSaOC8InesPYQPFwaMMX384NFd2pG2Ua0wVnrb3vIJGPLEgANAzp1CnaYPWpkdlvswkPixwYY2f7SQpEnkPB3zD1Kl7Q9ZRE1dizqGVapdHxhj4v4aPSEvE-LOigV56NFDGuo1HL6F8sMnJDUfzDFSjILzBmkoU34e0sTEU9nmHMjuimBHexZZ93ktuIAQA-aQM1EGi55lTVbrjBQQxWYwbn3s-YFM0MRPEg4TdoS2P3D4YKfBTAZ7UX82V2IsnCRsVeOHHbyxfK_adbuQJdLUjyi8JNivnC43rrL3j0hHnLzynGAwvKuw1F6jm0MGIJqWGOnJvHN6ThcdkBUmYx6Eijm6W4npoSd7NM3hxSouWmGrbwdZo7rh-tZlyRuHA)
 * [2020 - When BERT Plays the Lottery, All Tickets Are Winning](https://arxiv.org/pdf/2005.00561.pdf?fbclid=IwAR0tXWNR8Yn896ZTuDAxIVuDeK3YC1Cgnrj77kQgIvSaNPqCO9RtnhM31x0)
 

### 3. Large Language Models: Will they keep getting bigger? And, how will we use them if they do? - Luke Zettlemoyer

=> The Sparsely Gated mixt of experts
Modular language models
domain expert mixture

* Linguistic data are heterogeneous : news / medical / fiction .... 
* Adding experts and deleting them ?
* Zeroshot learning for string completion is really effective

* Papers of Luke around it :
 * [BASE Layers: Simplifying Training of Large, Sparse Models](https://arxiv.org/pdf/2103.16716.pdf)
 * [DEMix Layers: Disentangling Domains for Modular Language Modeling](https://openreview.net/pdf?id=BqgeyEMB-5)

### 4. Redesigning WSD with Extractive Sense Comprehension and Continuous Sense Comprehension - Edoardo Barba

* Edoardo Barba is a student of Navigli
* Meanings are following Zipf distrib too
* Plenty of class

Just using BERT and a Classifier is not effective :
* [ESC: Redesigning WSD with Extractive Sense Comprehension](https://aclanthology.org/2021.naacl-main.371.pdf) : 
Transformer based model for lexical meaning extraction based on dictionnaries
Contextualisation is power : use Context with word and context of others words + definition
* This model manage better rare sense

* Other interesting works of E. Barba :
 * [2021 - ConSeC: Word Sense Disambiguation as Continuous Sense
Comprehension](https://aclanthology.org/2021.emnlp-main.112.pdf) 
* [Exemplification Modeling: Can You Give Me an Example, Please?](https://www.diag.uniroma1.it/navigli/pubs/IJCAI_2021_Barbaetal.pdf)
* [ExtEnD: Extractive Entity Disambiguation](https://aclanthology.org/2022.acl-long.177.pdf)

### 5.  On the complementarity of neural and symbolic approaches, and on how to transfer between them - Eduard Hovy

=> Augmenting Babel with image description : [Retrieve, Caption, Generate: Visual Grounding for Enhancing Commonsense in Text Generation Models ](https://ojs.aaai.org/index.php/AAAI/article/download/21306/21055)
WSD via page rank
AMR 
SRL

* Bert and hyperonyms : Ok but just memorise...
* Bert & GPT3 : arithmetic : Ok but memorise...
* QA task : not using a fact but must infers

=> Is Bert just a smart table ?

* Other works of E. Hovy :
 * [Counterfactual Data Augmentation improves Factuality of Abstractive Summarization](https://arxiv.org/pdf/2205.12416.pdf) : augmentation with Wordnet hypernyms for summarisation
 * [Cross-Domain Reasoning via Template Filling](https://arxiv.org/pdf/2111.00539.pdf)
 * [Interpreting Deep Learning Models in Natural Language Processing:
A Review](https://arxiv.org/pdf/2110.10470.pdf)
 * 

### 6 -  What do neural vs neurosymbolic models learn? - Hinrich Schütze

NLU benchmark CODA 2021 (CoDA21: Evaluating Language Understanding Capabilities of NLP Models With Context-Definition Alignment(https://arxiv.org/pdf/2203.06228.pdf))
* Task : Define me a word definition  
* Best model based on simple distance metrics > Neural don't reason

* [Static Embeddings as Efficient Knowledge Bases?](https://arxiv.org/pdf/2104.07094.pdf) > they are on some tasks !
* Languages models as knowledge base ? underline differents issues :
 * entity ambiguity
 * rare entities 
 * nb of correct answer n!= 1 / n=0 / n>1
 => ranking could work but low
 
 * [BeliefBank: Adding Memory to a Pre-Trained Language Model for a Systematic Notion of Belief](https://arxiv.org/pdf/2109.14723.pdf)
  * adding memory with symbolic executive

Other interesting papers :
True Few-Shot Learning with Prompts—A Real-World Perspective(https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00485/111728)
(https://epub.ub.uni-muenchen.de/92448/)
The Reddit Politosphere: A Large-Scale Text and Network Resource of Online Political Discourse (https://ojs.aaai.org/index.php/ICWSM/article/view/19377/19149)
Geographic Adaptation of Pretrained Language Models(https://arxiv.org/abs/2203.08565)
Modular and Parameter-Efficient Multimodal Fusion with Prompting(https://arxiv.org/pdf/2203.08055.pdf)

## DAY 2 

### 1. Summary of the first day - Roberto Navigli

=> Meaning of human level in NLP ?
* Disagreement due to cultural / social 
* the question of interpretation
* Human can explain prediction
* Seriously need to revise data anotation process

=> Combining neural / symbolic systems ?
* Where integrating it in a neural system ? Decoding / fine tuning / retrivial system ?

=> How to build a KB ?
* manually ? NO !
* auto / semi-auto
* semantic parsing

=> Others remarks
* The problem of low resources
* Boostraping existing system ? More 
* The idea of a predicate repository

### 2. Neurosymbolic semantic parsing - Alexander Koller

The problem of compositional generalisation 
COGS corpus challenge :
* Seq to Seq not efficient on it => Not enough data ?

Seq2Seq good on lexical tasks but fails in synthaxic, semantic tasks. => one model > too much tasks ?

Am dependency parsing => allows to learn semantic dependancy tree
=> From tree to graph : use of AM algrebra 

Help to solve COGS  with a neural Barkler parser
Compositional Generalization Requires Compositional Parsers https://arxiv.org/pdf/2202.11937.pdf
Learning compositional structures for semantic graph parsing (https://arxiv.org/pdf/2106.04398.pdf)


### 3. Distilling conceptual knowledge from BERT - Steven Schockaert

Ruled based systems are also challenging : generally incomplete and generating from LM is noisy
=> need of flexible reasoning for interpolation (ex: Analogical reasoning)

Concept embeddings from BERT ? 
=> Inducing Relational Knowledge from BERT (https://www.ijcai.org/proceedings/2021/0530.pdf)
=> trying to infers differents relations (causality / Attribute / Lexical / Commonsense / Morphological) on DiffVec dataset

Masking concept is better than no mask during training step !

Distilling relation embeddings from pre-trained language models(https://arxiv.org/pdf/2110.15705.pdf)
* relation embeddings : vectors of pairs of words 
* better results with RoberTA

Relation vectors VS KB - how to deal with this duality ?

 
### 4. REBEL: Relation Extraction By End-to-end Language generation - Pere-Lluís Huguet Cabot 

Input : Raw text 
Output : entity relation entity sequence

* step 1 : Corpus creation crocodile based on TREX (wikipedia / Wikidata + NLI)
* step 2 : linearize dataset 
pre-training important 

for more info about this paper read this reading note : https://github.com/datalogism/ReadingsNotes/blob/main/Articles/2022_01_13_Rebel_navigli_cabot.md
